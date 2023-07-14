![image](https://github.com/xufeisofly/baby/assets/19555180/9737fda6-6af7-433a-a7ca-82b0527265f1)![image](https://github.com/xufeisofly/baby/assets/19555180/8ac4150c-0f56-4f8b-9a78-99e5a514d5c2)## 安装 qt5.12
现在只能去官网下载了，不过网盘里有。
选择 MSVC2015 MSVC2017
![image](https://github.com/xufeisofly/baby/assets/19555180/75b5daba-1685-44e0-85d7-15cddfe0f553)

## 安装 MSVC2017
下载 visual studio installer
![image](https://github.com/xufeisofly/baby/assets/19555180/1c6a6f6d-fae2-4c2b-90ad-7f24099e7f46)
![image](https://github.com/xufeisofly/baby/assets/19555180/6ef42353-e932-43d3-899f-ea8203a65997)

![image](https://github.com/xufeisofly/baby/assets/19555180/dda1d2fd-87df-441d-82d3-368d888da64a)
前面五个不用选，选择下面的 windows 10 SDK
同时在这里选择上 MSVC2015 MSVC2017(MSVC2019 可以不选, MSVC2015必须要选，不然 qt creator 无法识别 MSVC 的 compiler)
![image](https://github.com/xufeisofly/baby/assets/19555180/4a0808b7-ecae-4f3a-aa2f-4300f6c09bf3)

打开Qt Creator，在菜单栏依次选择：工具–>选项–>Kits–>编译器，如果你装了 MSVC2015 应该能自动识别出来，如图
![image](https://github.com/xufeisofly/baby/assets/19555180/19f05c00-7e48-4827-a07d-8006faa20108)
但是没有 MSVC2017，所以我们手动添加
![image](https://github.com/xufeisofly/baby/assets/19555180/cbc61a5a-1f53-4c31-b8b0-35a977360fcc)
![image](https://github.com/xufeisofly/baby/assets/19555180/123d18a5-28da-4a80-a7a6-25f72dcb7338)
找到 bat 文件路径，放进去，如C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\VC\Auxiliary\Build\vcvarsall.bat
![image](https://github.com/xufeisofly/baby/assets/19555180/953243f9-b630-4dda-8789-2676897ab3e8)
平台什么的按照上面的选择，之后填写脚本参数
如果你选择了 windows 10 SDK 10.0.20348.0, 那后面的参数就填写
x64 10.0.20348.0 -vcvars_ver=14.16

具体逻辑需要看 bat 文件里
![image](https://github.com/xufeisofly/baby/assets/19555180/95121133-79fa-4915-9fa5-af7e819f9945)

然后 kit 中选择这个 compiler 即可
![image](https://github.com/xufeisofly/baby/assets/19555180/7aabf95c-2134-4caa-9ccf-a45ac750e729)

## 安装 debug for windows
如果 kit 前面有个警告⚠符号，说明需要设置 debugger
这里下载 windows sdk setup.exe
https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/
在勾选的时候只选择 debugging for windows 就行了，其他都去掉，安装后警告符号就会消失




