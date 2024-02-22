# Lecture2_Notes   
# 第2节 轻松玩转书生·浦语大模型趣味Demo  宋志学   
[第2节课件Demo视频](https://www.bilibili.com/video/BV1Ci4y1z72H/?vd_source=427d5b3bd6552cd66c00e381e2aae338)  
[第2节Demo文档](https://github.com/InternLM/tutorial/blob/main/helloworld/hello_world.md)  

Lagent介绍
![](./lecture2_img1.png)  

模型下载
![](./lecture2_img2.png)  
![](./lecture2_img3.png)  
![](./lecture2_img4.png) 

### Hugging Face 模型下载
环境准备
  - 在internStudio平台中选择A100(1/4)的配置, 镜像选择`Cuda11.7-conda`
  - 进入开发机，打开终端，输入`bash` 过入`conda`环境
    ```
    bash # 请每次使用 jupyter lab 打开终端时务必先执行 bash 命令进入 bash 中
    bash /root/share/install_conda_env_internlm_base.sh internlm-demo  # 执行该脚本文件来安装项目实验环境
    ```
  - 激活环境
    ```conda activate internlm-demo```
    
  - 在环境中安装运行demo所需要的依赖

    ```
    # 升级pip
    python -m pip install --upgrade pip

    pip install modelscope==1.9.5
    pip install transformers==4.35.2
    pip install streamlit==1.24.0
    pip install sentencepiece==0.1.99
    pip install accelerate==0.24.1
    ```
通用环境配置  

pip换源  
```pip install -i https://mirrors.cernet.edu.cn/pypi/web/simple some-package```  

升级pip
```
python -m pip install --upgrade pip
pip config set global.index-url https://mirrors.cernet.edu.cn/pypi/web/simple
```
Conda 换源   

配置本地端口
```
ssh-keygen -t rsa
cat ~\.ssh\id_rsa.pub
ssh -CNg -L 6006:127.0.0.1:6006 root@ssh.intern-ai.org.cn -p 33090
```
 `33090` 是根据开发机的端口进行更改, 本机是 `36460`  

 Hugging Face 模型下载
```
 pip install -U huggingface_hub
huggingface-cli download --resume-download internlm/internlm-chat-20b --local-dir C:\Users\Dennis Chen  
```



