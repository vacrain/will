![image-20220428103906931](https://gitee.com/qzuser11/my_picture/raw/master/iamges/2022/2022-04-28_10-39-08_image-20220428103906931.png)

将外层的主要Index.html移动到src下，设为第一入口，其中playground/index 为第二入口

vite.config.ts配置如下

### 多页面使用时，vite配置项中注意点

1. 修改`root`参数为多页面的根目录：`./src/`，根据不同目录结构而修改

![image-20220428104240452](https://gitee.com/qzuser11/my_picture/raw/master/iamges/2022/2022-04-28_10-42-41_image-20220428104240452.png)

### 访问

页面一：`http://localhost:3000/`
页面二：`http://localhost:3000/playground/index.html`



# 以上为运行时环境配置







此部分为vite.config.ts 的打包配置



![image-20220428110227142](https://gitee.com/qzuser11/my_picture/raw/master/iamges/2022/2022-04-28_11-02-28_image-20220428110227142.png)

控制台运行 npm run build  

打包后路径为下



![image-20220428110321476](https://gitee.com/qzuser11/my_picture/raw/master/iamges/2022/2022-04-28_11-03-22_image-20220428110321476.png)

# 注

打包时把下面圈红的干掉，不要问什么，因为还没研究。。。

![image-20220428111457432](https://gitee.com/qzuser11/my_picture/raw/master/iamges/2022/2022-04-28_11-14-58_image-20220428111457432.png)



本地预览

npm run preview 

第一页  http://localhost:4173/

第二页  http://localhost:4173/playground