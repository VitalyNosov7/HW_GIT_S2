# Домашнее задание к уроку 2. Работа с изменениями
---

Данное домашнее задание является продолжением домашнего задания, которое вы выполняли на предыдущем семинаре в репозитории с собственным проектом.

1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.

3. Попробуйте отменить эти три коммита:
* последний — командами git reset --soft и git restore;
* предпоследний — командой git reset --mixed и git restore;
* первый — командой git reset --hard.

---
РЕШЕНИЕ:
---

1.   Для решения первой задачи были выполнены следующие команды:

         ```
         PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git log
         
         PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git diff 94e1a3107a447b39893aa691e939a4309f19c8c7 7e7a19134544b105f9c3e38d04e2f2a4c4f21562 d87583617148db199c8122f8432a008d14375674    
         ```

2.   Для решения второй задачи были выполнены следующие команды:

```
        PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git revert --no-commit d87583617148db199c8122f8432a008d14375674

        PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git revert --no-commit 7e7a19134544b105f9c3e38d04e2f2a4c4f21562

        PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git revert --no-commit 94e1a3107a447b39893aa691e939a4309f19c8c7

```

3.   Для решения третьей задачи были выполнены следующие команды:

```
    PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git reset --soft d87583617148db199c8122f8432a008d14375674

    PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git reset --mixed 7e7a19134544b105f9c3e38d04e2f2a4c4f21562
Unstaged changes after reset:
M       Program.cs
M       README.MD

    PS C:\Users\enot\Desktop\GIT\HW_GIT_S2> git reset --hard 94e1a3107a447b39893aa691e939a4309f19c8c7
```