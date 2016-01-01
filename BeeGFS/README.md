http://www.beegfs.com/wiki/ManualInstallWalkThrough

vagrant@node04:~$ sudo /etc/init.d/beegfs-client rebuild
- BeeGFS module autobuild
Building beegfs client module
{standard input}: Assembler messages:
{standard input}: Warning: end of file not at end of a line; newline inserted
{standard input}:886: Error: unbalanced parenthesis in operand 1.
gcc: internal compiler error: Killed (program cc1)
Please submit a full bug report,
with preprocessed source if appropriate.
See <file:///usr/share/doc/gcc-4.9/README.Bugs> for instructions.
scripts/Makefile.build:257: recipe for target '/opt/beegfs/src/client/beegfs_client_module_2015.03/build/../source/net/filesystem/FhgfsOpsRemoting.o' failed
make[3]: *** [/opt/beegfs/src/client/beegfs_client_module_2015.03/build/../source/net/filesystem/FhgfsOpsRemoting.o] Error 4
make[3]: *** Waiting for unfinished jobs....
Makefile:1395: recipe for target '_module_/opt/beegfs/src/client/beegfs_client_module_2015.03/build' failed
make[2]: *** [_module_/opt/beegfs/src/client/beegfs_client_module_2015.03/build] Error 2
Makefile:184: recipe for target 'module' failed
make[1]: *** [module] Error 2
AutoRebuild.mk:33: recipe for target 'auto_rebuild' failed
make: *** [auto_rebuild] Error 2

