# Basic Linter Setup

- reduce severity to warning stuff

```diff
{
-  "extends": ["tslint:recommended", "tslint-react", "tslint-config-prettier"],
+  "extends": [],
+  "defaultSeverity": "warning",
  "linterOptions": {
    "exclude": [
      "config/**/*.js",
      "node_modules/**/*.ts",
      "coverage/lcov-report/*.js"
    ]
  },
+  "rules": {
+    "semicolon": [true, "never"],
+    "interface-name": [true, "never-prefix"],
+    "noUnusedLocals": false
+  }
}
```
