# persp-mode-project-bridge

persp-mode project.el integration

## Installation

`M-x package-install-file RET persp-mode-project-bridge.el RET`

## How to configure

```elisp

    (with-eval-after-load "persp-mode-project-bridge-autoloads"
      (add-hook 'persp-mode-project-bridge-mode-hook
                (lambda ()
                    (if persp-mode-project-bridge-mode
                        (persp-mode-project-bridge-find-perspectives-for-all-buffers)
                      (persp-mode-project-bridge-kill-perspectives))))
      (add-hook 'after-init-hook
                (lambda ()
                    (persp-mode-project-bridge-mode 1))
                t))

```
