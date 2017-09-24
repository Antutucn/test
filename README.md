```java
<?xml version="1.0" encoding="utf-8"?>
<resources>

    <declare-styleable name="BouncingBallView">

        <attr name="ballCount" format="integer" /><!--小球的个数-->
        <attr name="ballColor" format="color" /><!--小球的颜色-->
        <attr name="ballRadius" format="dimension" /><!--小球的半径-->
        <attr name="cycleTime" format="integer" /><!--一个周期持续的时常-->
    </declare-styleable>
</resources>


private int mWidth = 300;//view的宽
    private int mHeight = 300;//view的高
    private int largeRadius;//(mWidth / 2 - ballRadius)

    private float wabbyBallX;//摇动中的小球x坐标
    private float wabbyBallY;//摇动中的小球y坐标
    private float wabbyBallStartAngle;//摇动的小球开始摇动的角度
    private float wabbyBallAngle;//摇动中小球的角度

    private float runningBallX;//转动小球的x坐标
    private float runningBallY;//转动小球的y坐标
    private float runningBallStartAngle;//转动小球开始转动的角度
    private float runningBallAngle;//转动中小球的角度

    private float perAngle;//将圆均分的角度
    private float restBallStartAngle = 60;//剩下的五个小球的开始分布的角度
    private float phaseAngle;//当两个小球碰撞时他们之间相差的角度

    private Paint mPaint;

    private STATUS currentStatus = STATUS.FIRSTCYCLE;

    private BouncingBallConfig config;//保存小球配置的类

    private enum STATUS {//运动状态的集合
        FIRSTCYCLE,
        RESTCYCLE
    }



```
