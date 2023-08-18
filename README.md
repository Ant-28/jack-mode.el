Jack Resources
==============

Contained here are resources for the nand2tetris "Jack" programming language.



Warning!
--------

For DOOM users, add the following Elisp to your `.config` file:

 
``` emacs-lisp

;; nand2tetris config for jack
(use-package! jack-mode
  :init
  (setq jack-tools-directory (concat nand2tetris-core-base-dir "/tools/"))
  (setq jack-build-directory "~/.emacs.d/.local/straight/jack-mode/libraries")


  )

(add-to-list 'auto-mode-alist '("\\.jack\\'" . jack-mode))

```
Optionally, configure this to run after any similar libraries, as required. 






Features
--------

- Unit testing framework "UnitTest".
    - Provides assertion functions for primitives and objects.
    - Provides detailed feedback for failing tests.
- String utility library aptly-dubbed "Strings".
    - `equals()`
    - `repeat()`
    - `join()`, `concat()`, `split()`
    - `coerceInt()`, `coerceChar()`, `coerceBoolean()`, `parseChar()`
    - `substring()`, `indexOf()`
    - `count()`
    - `sprintf()`
- Output sugar library named "Out".
    - Java-like `println()`
    - C-like `printf()`
    - `printfln()`
- Text-editor language support.
    - Emacs
        - Syntax highlighting including OS classes.
        - Compile `jack-build-directory` with `<f5>`.
        - Run the VMEmulator with `<f9>`.
