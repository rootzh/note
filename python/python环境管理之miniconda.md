## miniconda介绍
Miniconda 是一个轻量级的 Python 环境管理工具，基于 conda 包管理系统。它是 Anaconda 的简化版本，仅包含最核心的组件（如 conda、Python 及其依赖），用户可根据需要自行安装其他工具包

## 安装miniconda
1. windows命令提示符下执行命令：
   ```
   curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o .\miniconda.exe
start /wait "" .\miniconda.exe /S
del .\miniconda.exe
   ```
   安装后，打开“Anaconda Prompt (miniconda3)”程序以使用 Miniconda3。
2. windows power shell下执行命令：
   ```
   wget "https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe" -outfile ".\miniconda.exe"
Start-Process -FilePath ".\miniconda.exe" -ArgumentList "/S" -Wait
del .\miniconda.exe
   ```
   安装后，打开“Anaconda Powershell Prompt (miniconda3)”。
3. linux下安装
- 执行命令：
```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```
- 安装后，关闭并重新打开您的终端应用程序，或通过运行以下命令刷新它
```
source ~/miniconda3/bin/activate
```
- 然后，通过运行以下命令在所有可用 shell 上初始化 conda
```
conda init --all
```

## 常用命令
```
conda create -n env_name python=3.9	# 创建名为 env_name 的 Python 3.9 环境
conda activate env_name	# 激活指定环境
conda deactivate	# 退出当前环境
conda install numpy pandas	# 安装包（可指定版本，如 numpy=1.21）
conda list	# 查看当前环境已安装的包
conda remove -n env_name --all	# 删除指定环境
conda update conda	# 更新 conda 自身
conda env export > environment.yml  # 导出
conda env create -f environment.yml # 导入
```

默认环境存储在 ~/miniconda3/envs/，可通过 conda config 修改路径。

