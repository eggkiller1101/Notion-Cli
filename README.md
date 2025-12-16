- Language: Python
- TUI Framework: Textual
- Database: SQlite3 (further: SQLalchemy)
- Data format: SQL (further: JSON)
- Dependencies management: Poetry/pipenv
- Test: pytest
- Automatic flow: GitHub Actions

- PyInstaller打包位单文件发布到PyPI，提供Homebrew/Linux包

- 目前想到的难点（在终端中实现困难或不美观）：
1. 图片如何显示？
	- [image] placeholder + 系统图片查看
	给本地url和网络url两个路径，width和height是否要固定（暂定）
	拖拽/粘贴图片（支持）
	- 鼠标悬浮预览，好难暂不考虑
2. 不同格式工具作为扩展的支持？这个很难



- 核心功能：
1. 双向同步：连接Notion API
2. 导入/导出：什么格式？MD批量导入导出？CSV/JSON格式支持？
3. 全文搜索 SQLite FTS5扩展
4. 预置模板（TODO列表）
5. TUI界面
	- 三栏布局
	- 语法高亮（pygments集成）
	- 键盘快捷键自定义
	- 图片预览（通过kitty协议或chafa）
	- 暗色/亮色主题切换
6. 安全考虑
	- 凭证安全存储（keyring或加密文件）
	- SQLite数据库加密（SQLCipher)
	- 输入验证和防注入
7. 脚本扩展
	支持用户编写Python插件
8. git集成：笔记版本控制