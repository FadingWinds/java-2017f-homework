# 葫芦娃大战蝎子精  
## 实现功能
1. 编译完成后出现游戏界面；
2. 按下空格键开始游戏；
3. 回放功能调试良久未果（bug未消除），无奈将此部分移除。

## 程序框架
复用了以前的葫芦娃实验的基本框架，依照设计原则进行了一些改动，具体如下：
* `Main`类：程序的入口，继承了`JFrame`类；
* `Battlefield`类：绘图，继承了`JPanel`类；
* `Battle`类：游戏逻辑；
* `creatures`包
  * `Creature`类：抽象类，定义了所有生物的共同属性
  * `Grandpa`类：定义了爷爷的属性
  * `CalabashDoll`类：定义了葫芦娃的属性
  * `Scorpion`类：定义了蝎子的基本属性
  * `Soilder`类：定义了小喽啰的基本属性

## 设计原则  
### 单一职责原则
使每一个类只负责单一的功能。  
### 开放封闭原则  
父类的接口设置尽量满足对继承开放，对修改封闭。
### 里氏替换原则  
所有的Creature均可以被其子类型，如CalabashDoll、Grandpa等替换。  
游戏角色逻辑
1. 开局时，双方均摆一字长蛇阵；
2. 进攻开始，葫芦娃和小喽啰分别沿直线前进，二者相遇时，按照随机概率确定一个角色死亡；
3. 当葫芦娃或者小喽啰到达最后一列时，向中央聚集，先斩杀蝎子精\爷爷即可获得胜利。  

## 提交文件说明
1. CalabashDoll_Final文件夹为整个工程文件；
2. 葫芦娃大战蝎子精.mp4为某一次战斗的回放。
3. Readme.md为说明文档。