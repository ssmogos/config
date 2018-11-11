# keeper for tools configuration

## For emacs init.el, it's only needed to load use-package and point it to the config.org file:
``
(require 'package)
(setq package-enable-at-startup nil)
(add-to-list 'package-archives
	     '("melpa" . "https://melpa.org/packages/"))


;;initialize packages
(package-initialize)

;; Bootstrap `use-package'
(unless (package-installed-p 'use-package)
	(package-refresh-contents)
	(package-install 'use-package))


;; ssmogos configuration for emacs 
(org-babel-load-file (expand-file-name "~/dev/config/emacs/config.org"))
``


## For terminator, the sym link it to 
~/.config/terminator/config
