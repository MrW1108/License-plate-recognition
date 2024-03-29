# License plate recognition
License Plate RecognLicense plate recognitionition For Car With Python And OpenCV

#### 用python3+opencv3做的车牌识别系统，包括算法和客户端界面，只有2个文件，surface.py是界面代码，predict.py是算法代码

### 使用方法：
版本：python3.4.4，opencv3.4和numpy1.14和PIL5<br>
下载源码，并安装python、numpy、opencv的python版、PIL，运行surface.py即可

### 算法实现：
算法思想来自于网上资源，先使用图像边缘和车牌颜色定位车牌，再识别字符。车牌定位在predict方法中，为说明清楚，完成代码和测试后，加了很多注释，请参看源码。车牌字符识别也在predict方法中，请参看源码中的注释，需要说明的是，车牌字符识别使用的算法是opencv的SVM， opencv的SVM使用代码来自于opencv附带的sample，StatModel类和SVM类都是sample中的代码。SVM训练使用的训练样本来自于github上的EasyPR的c++版本。由于训练样本有限，你测试时会发现，车牌字符识别，可能存在误差，尤其是第一个中文字符出现的误差概率较大。源码中，我上传了EasyPR中的训练样本，在train\目录下，如果要重新训练请解压在当前目录下，并删除原始训练数据文件svm.dat和svmchinese.dat。

##### 额外说明：由于训练样本较少，误差较大。车牌定位算法的参数受图像分辨率、色偏、车距影响，有的车型识别效果有待提高。

##### 界面效果：
![](https://github.com/MrW1108/License-plate-recognition/blob/master/%5BSKG%605E%248~_RI7%7B%5DWEP5%25R1.png)
