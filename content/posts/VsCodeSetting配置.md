+++
title = 'VsCodeSetting配置'
date = 2024-11-12T21:31:17+08:00





categories = ["设置"] 

tags = ["setting" ]

+++



> 我的 `vscode` 的设置`.json`文件

# 2024.11.12 设置



```json
{
  "editor.fontSize": 16,
  "cph.general.autoShowJudge": false,
  "editor.formatOnSave": true,
  "editor.formatOnType": true,
  "files.autoSave": "afterDelay",
  "git.confirmSync": false,
  "chat.editor.fontSize": 18,
  "window.zoomLevel": 1,
  "editor.mouseWheelZoom": true,
  "editor.wordWrap": "on",
  "debug.onTaskErrors": "debugAnyway",
  "explorer.confirmDelete": false,
  "extensions.experimental.affinity": {
    "asvetliakov.vscode-neovim": 1
  },
  "workbench.settings.applyToAllProfiles": [
    "editor.fontSize"
  ],
  "go.delveConfig": {},
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[prisma]": {
    "editor.defaultFormatter": "Prisma.prisma"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.codeActionsOnSave": {
    "source.addMissingImports": "explicit",
    "source.organizeImports": "explicit"
  },
  "editor.cursorSmoothCaretAnimation": "on",
  "editor.cursorSurroundingLines": 5,
  "editor.fontFamily": "CaskaydiaCove Nerd Font",
  "editor.fontLigatures": true,
  "python.analysis.completeFunctionParens": true,
  "editor.fontSize": 18,
  "editor.fontWeight": "300",
  "editor.formatOnSave": true,
  "editor.inlineSuggest.enabled": true,
  "editor.lineNumbers": "relative",
  "editor.linkedEditing": true,
  "editor.smoothScrolling": true,
  "editor.stickyScroll.enabled": true,
  "editor.suggest.insertMode": "replace",
  "editor.suggestFontSize": 14,
  "editor.wordWrap": "on",
  "errorLens.fontStyleItalic": true,
  "everforest.italicKeywords": true,
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,
  "extensions.autoUpdate": "onlyEnabledExtensions",
  "extensions.ignoreRecommendations": false,
  "files.exclude": {
    "**/node_modules": true
  },
  "prettier.semi": false,
  "prettier.singleAttributePerLine": true,
  "prettier.singleQuote": true,
  "prettier.trailingComma": "all",
  "projectManager.git.baseFolders": [
    "$home/workspace"
  ],
  "projectManager.sortList": "Recent",
  "sortJSON.orderOverride": [
    "name",
    "version",
    "main",
    "module",
    "types",
    "typings",
    "files",
    "publishConfig",
    "repository",
    "scripts",
    "prefix",
    "description",
    "body"
  ],
  "sortJSON.orderUnderride": [
    "resolutions",
    "dependencies",
    "devDependencies",
    "peerDependencies",
    "cSpell.userWords"
  ],
  "typescript.preferences.importModuleSpecifier": "relative",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "update.showReleaseNotes": false,
  "vim.foldfix": true,
  "vim.highlightedyank.color": "rgba(230, 97, 89, 0.7)",
  "vim.highlightedyank.enable": true,
  "vim.highlightedyank.textColor": "white",
  "vim.hlsearch": true,
  "vim.leader": "<space>",
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": [
        "leader",
        "r"
      ],
      "commands": [
        "editor.action.rename"
      ]
    },
    {
      "before": [
        "leader",
        "w"
      ],
      "commands": [
        ":w!"
      ]
    },
    {
      "before": [
        "leader",
        "q"
      ],
      "commands": [
        ":q!"
      ]
    },
    {
      "before": [
        "leader",
        "x"
      ],
      "commands": [
        ":x!"
      ]
    },
    {
      "after": [
        "g",
        "g",
        "V",
        "G"
      ],
      "before": [
        "<c-a>"
      ]
    },
    {
      "before": [
        "<leader>",
        "k"
      ],
      "commands": [
        "editor.action.showHover"
      ]
    },
    {
      "before": [
        "[",
        "d"
      ],
      "commands": [
        "editor.action.marker.prev"
      ]
    },
    {
      "before": [
        "]",
        "d"
      ],
      "commands": [
        "editor.action.marker.next"
      ]
    },
    {
      "before": [
        "<leader>",
        "c",
        "a"
      ],
      "commands": [
        "editor.action.quickFix"
      ]
    },
    {
      "after": [
        "^"
      ],
      "before": [
        "H"
      ]
    },
    {
      "after": [
        "$"
      ],
      "before": [
        "L"
      ]
    },
    {
      "before": [
        "leader",
        "i"
      ],
      "commands": [
        "extension.toggleBool"
      ]
    }
  ],
  "vim.useSystemClipboard": true,
  "window.zoomLevel": 1,
  "workbench.iconTheme": "Monokai Pro Icons",
  "workbench.settings.editor": "json",
  "workbench.startupEditor": "readme",
  "zenMode.hideLineNumbers": false,
  "vsicons.dontShowNewVersionMessage": true,
  "[jsonc]": {
    "editor.quickSuggestions": {
      "strings": true
    },
    "editor.suggest.insertMode": "replace"
  },
  "terminal.integrated.defaultProfile.windows": "Command Prompt",
  "terminal.explorerKind": "external",
  "security.workspace.trust.enabled": false,
  "typescript.disableAutomaticTypeAcquisition": true,
  "git.enableSmartCommit": true,
  "git.openRepositoryInParentFolders": "always",
  "files.autoGuessEncoding": true,
  "code-runner.languageIdToFileExtensionMap": {
    "bat": ".bat",
    "powershell": ".ps1",
    "typescript": ".ts"
  },
  "vim.easymotion": true,
  // "editor.formatOnType": true,
  // "editor.formatOnSave": true,
  "go.formatTool": "gofmt",
  "[go]": {
    "editor.insertSpaces": true,
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.organizeImports": "explicit"
    },
    "editor.suggest.snippetsPreventQuickSuggestions": false
  },
  "animations.Install-Method": "Custom CSS and JS",
  "apc.imports": [
    "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.3/dist/updateHandler.js"
  ],
  "animations.CursorAnimation": true,
  "animations.CursorAnimationOptions": {
    "Color": "#ffb6c1",
    "TrailLength": 8
  },
  "animations.Smooth-Mode": false,
  "marscode.codeCompletionPro": {
    "enableCodeCompletionPro": true
  },
  "marscode.enableCodelens": {
    "enableInlineUnitTest": false,
    "enableInlineDocumentation": false
  },
  "vscode_custom_css.imports": [
    "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.4/dist/updateHandler.js"
  ]
}
```



