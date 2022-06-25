# l3luabridge

l3luabridge is an expl3 package for plain TeX and LaTeX that allows you to
execute Lua code in LuaTeX or any TeX engine that exposes the shell:

```
\documentclass{standalone}
\usepackage{l3luabridge}
\begin{document}
$ 1 + 2 = \luabridgeExecute{ print(1 + 2) } $
\end{document}
```

l3luabridge was previously part of the Markdown package, where it has been
battle-tested since 2016. Since 2022, l3luabridge has been available as a
separate package.
