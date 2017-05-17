# MessageBox
自定义的messageBox，可以报告详细信息错误。

、、、

    QMessageBox customMsgBox;
    customMsgBox.setWindowTitle(tr("警告消息提示！"));	//设置消息框的标题
    customMsgBox.setIconPixmap(QPixmap(":/res/resource/warning.png"));
    QPushButton *yesBtn=customMsgBox.addButton(tr("确定"),QMessageBox::ActionRole);
    customMsgBox.setText(QString("数据错误:%1! 程序即将关闭！").arg(errorMes));

    customMsgBox.exec();

    if(customMsgBox.clickedButton()== yesBtn)
        exit(0);
、、、
