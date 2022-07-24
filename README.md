# matlab_fdtd_GUI
Matlab -python -lumerical FDTD ，quick build the mode and access result data

基于matlab app设计的周期结构的光学快速建模计算和结果分析，由于接口通过python实现，需要python3.9或以上的环境（python需要装有numpy库），推荐anaconda(自动装好库)
[下载anaconda](https://www.anaconda.com/),同时需要matlab2022或以上版本以及lumerical FDTD2020以上版本（请安装在默认位置）  

初始化：  
打开MATLAB 2022，安装文件，第一次运行需要点击左上角小图标，选择python环境，例如D:\Anaconda\python.exe,再次打开即可运行。

实现的功能：
1，一键建模，打开文件后会自动读取fsp文件中的材料光参（如果需要添加材料可以预先在fsp文件中添加），添加层数，设置层的厚度，最后点击建模即可一键完成建模，点击运行会进入计算
2，光谱查看，文件计算完后可以在右边分析面板中选择查看反射透射光谱，程序会根据光谱自动算出吸收，可以选择展示选定线段，点击作图即可观看，
  同时如果打开的文件已经有计算结果，也可以直接在分析面板中查看，默认的监视器名称为'R','T','A',其中R和T的名称可以自由更改，可以选择输入想看的monitor  
3，场分布，右边分析面板可以获得分布图，输入monitor的名字，点击作图，可以获得场分布图，自动获得该monitor的点数，通过point条可以看不同的波长，下面的Interp可以实现场图的插值，
使图片更清晰。
