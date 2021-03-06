# Matlab
If you want to use, type `module load matlab`.

## GUI
You can use GUI matlab to explore small dataset or plot figures for your paper.

Warning: Do not use GUI mode to run large-scale experiment. GUI is run on managenode and will use all CPUs if parallelism is enabled. This will cause the unstability of the system.

If you connect the server via X11 or vnc desktop, you can start matlab by `proxychains4 matlab`.
![](./images/server_matlab.png)

## Non-GUI
Under nornal SSH login, you can invoke matlab by `proxychains4 matlab -nodesktop`. Notice this software is experimental supported by lab2c web admin.
Matlab may not start as you want.
![](./images/matlab_terminal.png)

## Script Mode
```shell
proxychains4 matlab -nodesktop -nosplash -nodisplay -r "run('path/to/your/script.m');exit;"
```

## Large Scale Computation
You can use `srun` to submit matlab job to compute node.