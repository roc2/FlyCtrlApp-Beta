            ---App V1.1     U30上位机
1、指令表
    24 4D 3C 00 64 64   MSP_IDENT       ---OK;
    24 4D 3C 00 65 65   MSP_STATUS      ---OK;
    24 4D 3C 00 66 66   MSP_RAW_IMU     ---OK;

    24 4D 3C 00 70 70   MSP_PID         ---OK;

    24 4D 3C 00 FE FE   MSP_DEBUG       ---OK;
    24 4D 3C 00 6D 6D   MSP_ALTITUDE    ---OK

24 4D 3C 00 64 64 24 4D 3C 00 70 70

24 4D 3C 00 64 64 24 4D 3C 00 65 65 24 4D 3C 00 66 66 24 4D 3C 00 70 70 24 4D 3C 00 FE FE 24 4D 3C 00 6D 6D


            ---App V1.9s
                    2016年8月19日11:12:33
1、在gyroscope.ui上面显示Acc和Gyro的数据和对应波形曲线

2、在u30.ui上显示U30的一些信息和PID

3、在baro.ui上显示气压计和Acc的数据和曲线

   24 4D 3C 00 68 68   MSP_MOTOR
   24 4D 3C 00 69 69   MSP_RC
   24 4D 3C 00 6F 6F   MSP_RC_TUNING

   24 4D 3C 00 68 68 24 4D 3C 00 69 69 24 4D 3C 00 6F 6F


13条指令：

24 4D 3C 00 64 64 24 4D 3C 00 73 73 24 4D 3C 00 65 65 24 4D 3C 00 66 66 24 4D 3C 00 67 67 24 4D 3C 00 68 68 24 4D 3C 00 69 69 24 4D 3C 00 6A 6A 24 4D 3C 00 6B 6B 24 4D 3C 00 6D 6D 24 4D 3C 00 6E 6E 24 4D 3C 00 FD FD 24 4D 3C 00 FE FE

4、可以显示遥控器数据

    ---App V2.0
        2016年8月22日09:35:53
1、马达的状态条顺时针竖着摆放

    ---App V2.2 ---OK
        2016年8月23日10:55:19
1.程序不会崩溃了

2.U30的PID、版本信息显示不正常

3、传感器数据无

4.修复程序崩溃问题、可以正常显示传感器数据
  在主界面中可以正常显示U30数据 、传感器的曲线正常
  数据可以正常解析、只有PID数据不能正常显示

    ---App V2.3
1、存在野指针 、程序运行一段时间后会崩溃

    ---App V2.4
        2016年8月25日16:30:47
1、 24 4D 3C 00 82 82     ---气压计数据
    24 4D 3C 00 E6 E6     ---滤波后的数据
    24 4D 3C 00 E7 E7     ---滑动加权滤波

    debug版本崩溃 用 release版

    ---App V2.5
1、卡尔曼滤波要过一会数据才有效 、大概两三分钟
   因为系数是自适应 、跟上一时刻和预测下一时刻的数据有关
   得多次递归接近平滑

2、加入加权滑动滤波



    ---App V2.6
1、filter.ui界面一个图里加入多条曲线显示

-----------------------------------遥控器APP-----------------------------------------------------

    ---App V1.3
1、可以正确解析遥控器发过来的数据
   遥控器发定值，上位机可以正确解析出来

    ---App V1.5
1、增加 progressbar显示对应的模式

2、显示遥控器发过来的数据

    ---App V1.6
1、可以显示飞控数据、还有遥控器的数据

2、和MWC的显示的数据基本一样 、PID的第十组数据对不上

3、仿了一下，PID的数据全部正确、MWC的第十组PID对不上
































