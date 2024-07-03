# Changes

## 2.2.0 (2024-07-03)

Development:

- Automatically determine value of `\c_luabridge_default_output_dirname_str`
  based on the current output directory.
  (witiko/markdown#457, #26, #27, reported by @hongy19)

Continuous Integration:

- Automatically test the library on both Linux and Windows.

## 2.1.0 (2024-02-14)

Development:

- Define function `\luabridge_tl_set:Nn`.

## 2.0.2 (2022-10-24)

Fixes:

- Fix tokenization in error-reporting code. (#17, #19)
- Catch compilation errors in TeX engines other than LuaTeX. (#18, #20)

Refactoring:

- Remove useless uses of `\l_tmpb_tl`. (24e116d)

## 2.0.1 (2022-08-16)

Fixes:

- Apply proper error handling when executing Lua via shell escape. (#15)

## 2.0.0 (2022-08-08)

Breaking Changes:

- Use `\sys_get_shell:nnNTF` from l3sys instead of `\immediate\write18` and
  `os.execute()`. (#13)
    - Merges `\c_luabridge_method_write_eighteen_int` and
      `\c_luabridge_method_os_execute_int` into
      `\c_luabridge_method_shell_int`.
    - Removes `\g_luabridge_standard_output_filename_str` and
      `\c_luabridge_default_standard_output_filename_str`.

Fixes:

- Execute chunks that end with `end` or a Lua comment. (#11, #14)
- Sandbox direct Lua access. (#11, #14)
- Make nested calls defined behavior. (#8, #13)

Refactoring:

- Remove needless whitespaces in Lua code.
- Replace (plain) TeX primitives with `\iow_*` l3file functions. (#1, #3,
  latex3/latex3#1105, latex3/latex3#1114. latex3/latex3#1117)
    - Many thanks to @josephwright, @u-fischer, and @FrankMittelbach at
      latex3/latex3#1114, and Hans Hagen, @hmenke, and @mojca at
      [dev-context][1] for helping to make l3file compatible with ConTeXt MkII.

 [1]: https://mailman.ntg.nl/pipermail/dev-context/2022/003912.html
      (A robust way of detecting ConTeXt from LaTeX3)

## 1.0.1 (2022-06-27)

This release includes PDF documentation of lt3luabridge.

## 1.0.0 (2022-06-26)

Initial release
