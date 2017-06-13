`id:000000,sig:06,src:004494,op:havoc,rep:2`

stdout: `gravity: src/compiler/gravity_codegen.c:646: void visit_empty_stmt(gvisitor_t *, gnode_empty_stmt_t *): Assertion `(context_object->isa == gravity_class_function)' failed.`

```
#0  0x00007f3ceabb6067 in __GI_raise (sig=sig@entry=6) at ../nptl/sysdeps/unix/sysv/linux/raise.c:56
56      ../nptl/sysdeps/unix/sysv/linux/raise.c: No such file or directory.
(gdb) bt
#0  0x00007f3ceabb6067 in __GI_raise (sig=sig@entry=6) at ../nptl/sysdeps/unix/sysv/linux/raise.c:56
#1  0x00007f3ceabb7448 in __GI_abort () at abort.c:89
#2  0x00007f3ceabaf266 in __assert_fail_base (fmt=0x7f3ceace7f18 "%s%s%s:%u: %s%sAssertion `%s' failed.\n%n", assertion=assertion@entry=0x492c96 "(context_object->isa == gravity_class_function)", file=file@entry=0x492c24 "src/compiler/gravity_codegen.c",
    line=line@entry=646, function=function@entry=0x4933a0 "void visit_empty_stmt(gvisitor_t *, gnode_empty_stmt_t *)") at assert.c:92
#3  0x00007f3ceabaf312 in __GI___assert_fail (assertion=0x492c96 "(context_object->isa == gravity_class_function)", file=0x492c24 "src/compiler/gravity_codegen.c", line=646, function=0x4933a0 "void visit_empty_stmt(gvisitor_t *, gnode_empty_stmt_t *)") at assert.c:101
#4  0x0000000000407a47 in visit_empty_stmt (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_codegen.c:646
#5  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#6  0x0000000000409712 in visit_class_decl (self=0x7fffc9a09fc8, node=0x2255c70) at src/compiler/gravity_codegen.c:1105
#7  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#8  0x0000000000408509 in visit_variable_decl (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_codegen.c:952
#9  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#10 0x0000000000405ba5 in visit_compound_stmt (self=0x7fffc9a09fc8, node=0x2258590) at src/compiler/gravity_codegen.c:298
#11 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#12 0x0000000000409023 in process_getter_setter (self=0x7fffc9a09fc8, p=<optimized out>, c=<optimized out>) at src/compiler/gravity_codegen.c:844
#13 visit_variable_decl (self=0x7fffc9a09fc8, node=0x22541b0) at src/compiler/gravity_codegen.c:1006
#14 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#15 0x0000000000409712 in visit_class_decl (self=0x7fffc9a09fc8, node=0x2253fe0) at src/compiler/gravity_codegen.c:1105
#16 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#17 0x0000000000408509 in visit_variable_decl (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_codegen.c:952
#18 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#19 0x0000000000407f0d in visit_function_decl (self=0x7fffc9a09fc8, node=0x2253ce0) at src/compiler/gravity_codegen.c:890
#20 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#21 0x0000000000405992 in visit_list_stmt (self=0x7fffc9a09fc8, node=0x2251db0) at src/compiler/gravity_codegen.c:292
#22 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#23 0x000000000040558e in gravity_codegen (node=0xfa5, delegate=0x7fffc9a0a188, vm=0x2252390) at src/compiler/gravity_codegen.c:1879
#24 0x0000000000437b62 in gravity_compiler_run (compiler=0x2252330, source=<optimized out>, len=<optimized out>, fileid=<optimized out>, is_static=<optimized out>) at src/compiler/gravity_compiler.c:175
#25 0x0000000000491e8a in main (argc=<optimized out>, argv=<optimized out>) at src/cli/gravity.c:197
```





`id:000001,sig:11,src:004341,op:havoc,rep:4`

```
#0  0x000000000040e0fd in report_error (self=<optimized out>, node=0x0, format=<optimized out>) at src/compiler/gravity_codegen.c:79
#1  0x000000000040ee26 in store_declaration (self=0x7fffa65e3528, obj=<optimized out>, is_static=<optimized out>, node=0x0) at src/compiler/gravity_codegen.c:662
#2  0x000000000040979f in visit_class_decl (self=0x7fffa65e3528, node=0x2466980) at src/compiler/gravity_codegen.c:1114
#3  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#4  0x0000000000408bd8 in visit_variable_decl (self=0x7fffa65e3528, node=0x246e800) at src/compiler/gravity_codegen.c:1048
#5  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#6  0x0000000000409712 in visit_class_decl (self=0x7fffa65e3528, node=0x2465d30) at src/compiler/gravity_codegen.c:1105
#7  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#8  0x0000000000408509 in visit_variable_decl (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_codegen.c:952
#9  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#10 0x0000000000407f0d in visit_function_decl (self=0x7fffa65e3528, node=0x24649d0) at src/compiler/gravity_codegen.c:890
#11 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#12 0x0000000000405992 in visit_list_stmt (self=0x7fffa65e3528, node=0x2461db0) at src/compiler/gravity_codegen.c:292
#13 0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#14 0x000000000040558e in gravity_codegen (node=0x4932b2, delegate=0x7fffa65e36e8, vm=0x2462d20) at src/compiler/gravity_codegen.c:1879
#15 0x0000000000437b62 in gravity_compiler_run (compiler=0x2462cc0, source=<optimized out>, len=<optimized out>, fileid=<optimized out>, is_static=<optimized out>) at src/compiler/gravity_compiler.c:175
#16 0x0000000000491e8a in main (argc=<optimized out>, argv=<optimized out>) at src/cli/gravity.c:197
```





`id:000005,sig:11,src:004637+001656,op:splice,rep:2`

```
#0  symboltable_lookup (table=0x2, identifier=0x11843b0 "f1") at src/compiler/gravity_symboltable.c:117
#1  0x00000000004296d7 in check_class_ivar (self=<optimized out>, classnode=<optimized out>, node=<optimized out>) at src/compiler/gravity_semacheck2.c:497
#2  visit_class_decl (self=0x7fff28e8c148, node=0x1183f90) at src/compiler/gravity_semacheck2.c:874
#3  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#4  0x00000000004282a2 in visit_variable_decl (self=0x7fff28e8c148, node=0x1184ce0) at src/compiler/gravity_semacheck2.c:772
#5  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#6  0x00000000004279da in visit_function_decl (self=0x7fff28e8c148, node=0x1183c50) at src/compiler/gravity_semacheck2.c:729
#7  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#8  0x0000000000425563 in visit_list_stmt (self=0x7fff28e8c148, node=0x1181db0) at src/compiler/gravity_semacheck2.c:532
#9  0x0000000000403247 in gvisit (self=<optimized out>, node=<optimized out>) at src/compiler/gravity_visitor.c:33
#10 0x00000000004251fa in gravity_semacheck2 (node=0x2, delegate=0x7fff28e8c2d8) at src/compiler/gravity_semacheck2.c:1189
#11 0x0000000000437b22 in gravity_compiler_run (compiler=0x1181f40, source=<optimized out>, len=<optimized out>, fileid=<optimized out>, is_static=<optimized out>) at src/compiler/gravity_compiler.c:171
#12 0x0000000000491e8a in main (argc=<optimized out>, argv=<optimized out>) at src/cli/gravity.c:197
```



