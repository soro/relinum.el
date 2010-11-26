Relinum
=======

As it says in the description, this mode is basically linum-mode by Markus Triska, modified to provide relative line numbers. I called it relinum so it can coexist with normal linum-mode.
I wasn't able to find a package that provided relative line numbers and since I like to use Viper and Vimpulse, I was sorely missing this feature.
This is in fact even better than the Vim version, since it will number both windows that show the same buffer and will even work if you use <code>follow-mode</code>.

Issues
------

Currently there is one problem that depending on your taste could be minor or really annoying. If line-wrapping is turned on and the same buffer is viewed in 2 windows at the same time, sometimes the point jumps to the middle of the screen and the screen stays fixed instead of scrolling. For this reason I have decided to automatically turn off line wrapping if the mode is loaded.

If anyone has an idea why this happens or how to fix it, please send me a patch. 
In the past I have encountered this problem when using <code>highlight-parentheses-mode</code>, so I don't think it is an issue with my code.

Installation
------------

To install, either clone this repository or download relinum.el, put it somewhere on your load path and add <code>(require 'relinum)</code> to your emacs config. You can load the mode via <code>M-x relinum-mode</code> or globally enable it via <code>M-x global-relinum-mode</code>.
