# projectdemo
projectdemo



```
graph TD
A[Activity 启动]-->B[onCreate]


B[onCreate]-->C[onStart]


C[onStart]-->D[onResume]


D[onResum]-->E[Activity 运行]


E[Activity 运行]-->|新Activity启动|F[onPause]


F[onPause]-->|Activity已经不可见|G[onStop]


K-->|用户返回原Activity|B[onCreate]


F-->|用户返回原Activity|D


G[onStop]-->|Activity正在停止或者即将被销毁|H[onDestroy]




G-->|高优先级的应用需要内存|K[应用被杀死]




G-->|用户返回原Activity|L[onRestart]


H[onDestroy]-->I[Activity 销毁]


L-->C




```
