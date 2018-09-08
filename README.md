# piuitext1
先用qtcreator画了个ui，转换成.py方便后期编程，因为少爷我C++比较次，过程如下：

 1.qtcreator画完之后保存会得到一个.ui文件，其实就是你画的界面，把地址复制好。
 2.因为我Python的编译器是pycharm，如想用pycharm编qt当然需要pyqt（我印象里如果你环境是anaconda他自带pyqt这里我印象不深，上学期的事儿了），
安装后会出现D:\anaconda3\Lib\site-packages\PyQt5\uic 这个路径（根据自己地址改）。
 3.在cmd中进入该文件夹，然后敲pyuic5 -o destination.py source.ui 根据自己qt版本改成pyuic4或者其他，后面第一个文件时输出的py文件，后面是你画的ui文件，
两者都可以在前面加路径。
 4.还有一个修改工作 在引用的地方加上import sys
 5.结尾加上if __name__ == "__main__":
    app = QtWidgets.QApplication(sys.argv)
    MainWindow = QtWidgets.QMainWindow()
    ui = Ui_MainWindow()
    ui.setupUi(MainWindow)
    MainWindow.show()
    sys.exit(app.exec_())
 就可以可以用编译器的开了，也可以显示你的界面了。
 6.参考文献https://www.jianshu.com/p/43300f85af3e
