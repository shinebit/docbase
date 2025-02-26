`rsync`是一个非常强大的文件同步工具，常用于在本地和远程计算机之间传输和同步文件。它支持增量备份，能够只传输更改过的文件部分，因此非常高效。

### 基本命令格式
```bash
rsync [options] source destination
```

### 常用参数
- `-a`  
启用归档模式，等同于`-rlptgoD`，会递归复制文件，并保留符号链接、权限、时间戳、组、所有者和设备文件等元数据。

- `-v`  
显示详细输出，列出正在复制的文件和目录。

- `-z`  
启用压缩，减少数据传输量，适用于带宽较低的网络。

- `--delete`  
删除目标目录中源目录中不存在的文件（确保目标目录和源目录保持一致）。

- `-e`  
指定远程 shell 命令（例如使用 SSH）。常用于设置远程传输时的连接方式。

### 示例命令
基本本地备份
```bash
rsync -av /source/ /destination/
```

删除目标中不存在于源目录的文件
```bash
rsync -av --delete /source/ /destination/
```

远程备份（使用 SSH）
```bash
rsync -av -e ssh /source/ user@remote:/destination/
```
