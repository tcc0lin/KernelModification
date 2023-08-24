# KernelModification

配合改机策略所做的内核层函数修改
- maps展示内容特征修改
    - fs/proc/task_mmu.c->show_map_vma()
- stat属性修改
    - fs/stat.c->SYSCALL_DEFINE4(newfstatat)
- statfs属性修改
    - fs/statfs.c->SYSCALL_DEFINE2(statfs)
- uname信息修改
    - kernel/sys.c->SYSCALL_DEFINE1(newuname)
- getdents某些文件隐藏（针对ext4类型的目录）
    - fs/ext4/dir.c(ext4_readdir)