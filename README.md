# Linux Kernel
Self compiled Linux Kernel
- Used BusyBox for Linux utilities and Qemu as a hypervisor
- Total file size went to 68Mb

![Linux Compiled](https://pbs.twimg.com/media/GJDeJprXcAABiHK?format=jpg&name=large)

## Steps to run
1. Clone the repo
    ```sh
    git clone git@github.com:pranjal-barnwal/linux-kernel.git
    ```

2. Move to the `linux-kernel` directory
    ```sh
    cd linux-kernel
    ```

3. Install ***QEMU***, which will be used as Hypervisor for our  kernel. You can download it from [here](https://qemu.weilnetz.de)

4. Set up the path environment variable in your windows system. Add the below path:
    ```pwsh
    C:\Program Files\qemu
    ```

5. Then we can simply boot up the image using
    ```pwsh
    qemu-system-x86_64 boot
    ```

6. New window will be popped asking what to boot. Then we need to pass file path in that window:
    ```pwsh
    /bzImage -initrd=/init.cpio
    ```

7. That's it, CLI interface will be loaded and we're good to go.

<br>


    NOTE: All the linux commands will not be working, since all binaries for the commands are not present

![Ciao!](https://y.yarn.co/dba502c0-ff26-437c-8211-22e0421e42f0_text.gif)