# react-ts-boilerplate
原博：https://juejin.cn/post/6844904055618158600

# 1 dotfiles

dotfiles是指项目中以`.`开头的配置文件

## 1.1 .gitignore

- 安装gitignore插件，`ctrl+shift+p`呼出命令面板，执行`Add gitigore`命令，然后选择不同类型项目的ignore配置，可以多次追加。

- 这个扩展的原理是通过拉取开源项目 [gitignore](https://link.juejin.cn/?target=https%3A%2F%2Fgithub.com%2Fgithub%2Fgitignore) 的 `gitignore` 配置，所以要保证扩展运行时的网络质量

  > 如果遇到connect ECONNREFUSED 0.0.0.0:443的错误，可以尝试将https://github.com/googlehosts/hosts中的hosts文件替换本地的hosts文件（~/etc/hosts）

- 本次选择添加的项目类型包括：`Node`, `VisualStudioCode`, `JetBrains`, `Windows`, `Linux`, `macOS`，可以根据自己的需要添加其它的项目类型例如 `SublimeText`，`Vim`。

## 1.2 .editorconfig

- 用于帮助开发人员在不同IDE下**初步统一**代码格式
- 在这里配置的代码规范规则优先级高于编辑器默认的代码格式化规则。
- 只能简单的配置一些规范，并不能完全满足代码规范的需求，所以还需要其它代码检查工具配合使用，比如ESLint或StyleLint，统一代码风格。
- 使用
  - 安装`EditorConfig for VSCode`插件，辅助VSCode读取配置
  - 新建`.editorconfig`文件，编写规则即可

## 1.3 .nvmrc

`.nvmrc` 是 `nvm` 的配置文件，很多工具在判断项目的 node 版本的时候会读取其中的node版本

```shell
node --version > ./.nvmrc
```

## 1.4 .vscode

- `.vscode/settings.json`：VSCode编辑器设置
- `.vscode/extensions.json`：推荐的扩展，如未安装，就会自动提示用户安装

## 1.5 package.json

包管理文件，`yarn init -y`即可一键生成
