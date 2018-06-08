# 使用canvas绘制贝塞尔曲线 


### 贝塞尔曲线原理 图示如下：

![贝塞尔曲线原理图]("https://github.com/nixinyudada/beziercurve/raw/master/img/biziercurve.png");


```javascript
var canvas=document.getElementById('canvas');
var context=canvas.getContext('2d');
```

1. 绘制起始点、控制点、终点 (P0,P1,P2,P3)	

```javascript
context.beginPath();  // start
context.moveTo(25,175);   // P0
context.lineTo(60,30);   // 控制点 P1
context.lineTo(170,30);  // 控制点 P2
context.lineTo(170,175);  // P3
context.stroke();   // end
```

2. 绘制3次贝塞尔曲线

```javascript
context.beginPath(); 
context.moveTo(25,175);   // 端点 P0
context.bezierCurveTo(60,30,170,30,170,175);  // 依次为 P1 P2 P3 
context.strokeStyle = "red";   // curve's fill color
context.stroke();   // end
```
