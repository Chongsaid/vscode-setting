# VSCode 配置说明

> Author : Chongsaid
>
> Date : 2020-07-24 10:00
>
> Version : 1.0
>
> Tips : 若部分配置不清楚，可移动鼠标至配置上，即可获取相应讯息



`注意`：配置文件显示的注释红色背景并不会影响配置，因此请放心将一整个文件的内容复制到你的 setting.json 中以配置，而这些注释也能帮助你进行个性设置。



``` javascript
{

  // ************************************************************
  // * @author Chongsaid
  // * @date 2020-07-24 10:00
  // * version 1.0
  // * Tips：若部分配置不清楚，可移动鼠标至配置上，即可获取相应讯息
  // ************************************************************

  
  // -------------------------------------------------------------------
  // | 推荐：安装插件列表 -> 通常注明对应的开发语言，你可以选择所需的
  // |
  // | 注意：首先安装所需插件，再复制此份配置表至 setting.json 中
  // |      如果显示错误讯息，则可能是没有相应的插件支持，此时也可以注释掉它们
  // --------------------------------------------------------------------

  // ***************************************
  //           插件列表 version 1.0
  // ***************************************
  // -> Language Support 
  //  
  //  => 简体中文支持
  //     1. Chinese (Simplified) Language Pack for Visual Studio Code 
  //
  // -> ICON Theme
  // 
  //    1. Material Icon Theme (本配置默认使用)
  //    2. vscode-icons
  // 
  // -> Color Theme（可选择安装一个合适的主题，例如大多数人喜欢暗黑模式，若你有合适的，可编辑加入）
  //
  //    1. Horla Light Theme（本配置默认使用）
  //    2. Material Theme（有多种黑暗模式的主题哦）
  //
  //
  // -> Java SpringBoot Support
  //  
  //  1. Spring Boot Extension Pack
  //  依赖项（附带安装）
  //      Spring Boot Tools
  //      Concourse CI Pipeline Editor
  //      Cloudfoundry Manifest YML Support
  //      Spring Initializr Java Support
  //      Spring Boot Dashboard
  // 
  //  2. Java Extension Pack
  //  依赖项（附带安装）
  //      Language Support for Java(TM) by Red Hat
  //      Debugger for Java
  //      Java Test Runner
  //      Maven for Java
  //      Java Dependency Viewer
  //      Visual Studio IntelliCode
  //
  //
  //
  // ************************************************************
  // *                        待更新                             *
  // ************************************************************






  // ----------------------------------------
  // | 通用配置 -> 通常是用于主题或编辑器的配置
  // ----------------------------------------

  
  "vsicons.dontShowNewVersionMessage": false,
  // VsCode 图标主题
  "workbench.iconTheme": "material-icon-theme",
  // VSCode 颜色主题
  "workbench.colorTheme": "Horla",
  "editor.fontSize": 14.5,
  "editor.tabSize": 2,


  "terminal.integrated.cursorStyle": "line",

  "files.exclude": {
    "**/.classpath": true,
    "**/.project": true,
    "**/.settings": true,
  },


  // -------------------------------------------------------
  // | 字体配置 -> 通常是配置编辑器以及终端，控制台，界面的字体
  // -------------------------------------------------------

  // 推荐使用此字体 window 推荐 consolas, Ubuntu 推荐 monospace

  "terminal.integrated.fontWeightBold": "normal",
  "terminal.integrated.fontFamily": "monospace",

  "editor.fontFamily": "monospace,Consolas,'Droid Sans Mono', 'monospace', monospace, 'Droid Sans Fallback'",
  "editor.fontLigatures": true,
  
  "markdown.preview.fontFamily": "-apple-system, monospace, BlinkMacSystemFont, 'Segoe WPC', 'Segoe UI', system-ui, 'Ubuntu', 'Droid Sans', sans-serif",

  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "name": "Comment",
        "scope": [
          "comment",
          "comment.block",
          "comment.block.documentation",
          "comment.line",
          "comment.line.double-slash",
          "punctuation.definition.comment",
        ],
        "settings": {
          // 字体样式：空表示 normal -> 不粗体不斜体
          "fontStyle": ""
        }
      },
    ]
  },



  // -----------------------------------------------------------------------
  // | 环境配置 -> 通常是用于某程序依赖于某个运行环境的配置：如 Java 依赖虚拟机（JDK）
  // -----------------------------------------------------------------------

  // 通常是需要 JDK11 作为主环境
  "java.home":"/usr/local/java/jdk-11.0.8",

  // Maven user setting 所在位置以及 Maven 命令（mvn）所在路径（ Window的是 mvm.cmd ） 
  "java.configuration.maven.userSettings":  "/home/matrix/rely/apache-maven-3.6.3/conf/settings.xml",
  "maven.executable.path": "/home/matrix/rely/apache-maven-3.6.3/bin/mvn",

  // maven 在终端使用的 java.home -> 具体请移动鼠标至键中，视情况，我使用的是 JDK11
  "maven.terminal.useJavaHome": false,

  // 自定义环境变量 -> 其实是多余的，视情况使用
  "maven.terminal.customEnv": [
      {
          "environmentVariable": "JAVA_HOME",
          "value": "/usr/local/java/jdk-11.0.8"
      }
  ],
  
  // 配置 JDK 运行环境并指定一个默认的（JDK8）
  "java.configuration.runtimes": [
    {
      "name": "JavaSE-1.8",
      "path": "/usr/local/java/jdk1.8.0_261",
      "default": true
    },
    {
      "name": "JavaSE-11",
      "path": "/usr/local/java/jdk-11.0.8",
    }
  ],


  // -----------------------------------------------------------------------
  // | 编程语言控制 -> 通常是用于配置程序的格式化，语义，检查语法等讯息
  // -----------------------------------------------------------------------

  // Java 语义突出显示
  "java.semanticHighlighting.enabled": true,
  

  // 当安装了针对某款语言的插件时，如该插件提供了格式化等选项，可以将下方注释解除以配置

  //"[javascript]": {
  //  "editor.defaultFormatter": ""
  //},

  
  
  // -----------------------------------------------------------------------
  // | 其它配置 -> 应谨慎的查看各处配置的作用，否则不应该去修改它们
  // -----------------------------------------------------------------------

  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
  "editor.suggestSelection": "first",
  "editor.semanticTokenColorCustomizations": null

}
```

