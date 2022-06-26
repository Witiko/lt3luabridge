# l3luabridge

 [![license](https://img.shields.io/github/license/witiko/markdown)](LICENSE)
 [![ci](https://github.com/witiko/l3luabridge/actions/workflows/main.yml/badge.svg)][4]

l3luabridge is an [expl3][1] package that allows you to execute Lua code in
LuaTeX or any TeX engine that exposes the shell:

``` tex
\documentclass{standalone}
\usepackage{l3luabridge}
\begin{document}
$ 1 + 2 = \luabridgeExecute{ print(1 + 2) } $
\end{document}
```

l3luabridge was previously part of [the Markdown package for TeX][2], where it
has been battle-tested since 2016. [Since 2022][3], l3luabridge has been
available as a separate package.

 [1]: http://mirrors.ctan.org/macros/latex/contrib/l3kernel/expl3.pdf
 [2]: https://www.ctan.org/pkg/markdown
 [3]: https://github.com/witiko/markdown/pull/141
 [4]: https://github.com/Witiko/l3luabridge/actions
