

- 如果问,指针需要什么才能学会?

- 我想,一部电话就够了.

<!--more-->

欢迎跳过婆婆妈妈吗的环节,点我传送到!!!正文!!!

# 照常唠嗑

去年(2018年),在学校某实验室中我做了一次公开分享,完成了<<指针:兰花指到弹指神通>>.第一稿通过提出指针模型让很多同学重新认识了指针和C语言.年终总结的时候,我再次回顾我的文章,发现它只能起到启发理解作用,但文章缺少了系统条理性和易理解性.

![u=2712757308,2019535597&fm=26&gp=0.jpg](https://i.loli.net/2019/01/04/5c2efcd12621b.jpg)

于是我把<<指针:兰花指到弹指神通>>的第二稿<<C指针:指点江山>>列入了2019的计划中去,希望在不降低文章的幽默性的前提下,将指针的理解层次进一步深化.

![u=3316908823,1055879217&fm=26&gp=0[1].jpg](https://i.loli.net/2019/01/04/5c2efbb865090.jpg)

本稿由莫斯担任主编.具体参加本稿编写的有莫斯莫死.全稿由莫斯莫死统稿并审定.限于(咸鱼)水平和时间,书中难免有纰漏之处,敬请谅解.殷切期待读者和专家学者批评赐教.

## 关于上一稿

如果让我评价上一稿的话,一个词:**狗屁不通**

## 恐惧起源

为什么对指针指针感到恐惧?

事实上,对任何未知的事物我们都会感到恐惧.

指针方便了计算机找到以它为地址的内存单元.

内存单元,地址,计算机...一个个生僻的名词.

现在你应该知道为什么你总是理解不了指针了吗?

你以为是背景知识不够,不,并不是!

因为这些名词哪条和你有关系?

本文完

开个玩笑,指针确实和我们关系不太大,因为他方便的计算机而并非使用计算机的人,所以在其他程序设计语言中你很少会看到出现指针这么一说.

所以在传统的学习指针过程中,教材把你当成计算机去教,你也真敢跟教才着去学,那当然最后竹篮打水一切皆空.

无论是考试也好,工作也罢,知识要为自己服务,自己要最终为人民服务,投身到社会主义建设的浪潮中去.

## 宇宙中最伟大的神

林俊杰的不为谁而作的歌MV最后讲到,宇宙中最伟大的神和最渺小的神同名,他们叫做谢谢.

在这里感谢所有为本稿编写做出贡献的人.
 
感谢来听我讲课的同学们，他们帮助我发现错误，提出了改进意见，并在教学过程忍受着草稿形式的教材。他们对我的作品反应向我提供了有益的帮助。  

我还要感谢我们班级的管理人员，校科协的管理人员，Python大数据实验室的管理人员，他们提供给我了一次次展示自己的机会，提出了许多有价值的建议。  

啰啰嗦嗦终于把唠嗑部分写完了.如果您看着烦,别抱怨我写这部分和您有同样的烦恼!   

<p align="right">莫斯莫死(MossNoDie)</p>
<p align="right">moss@nodie.ink</p>


# `chapter[1].name=”愤怒的送餐员\0”`
实验室的一个朋友李刚刚码了一上午代码，有些饿了，于是在网上定了一个外卖，送餐员给他打电话问送到哪时。“送到一个黑衣服黑裤子的人手里。”李刚刚说。送餐员气愤的挂掉了电话。
![愤怒的送餐员](https://t.cn/E4zP6DZ)

## `(chapter+1)->(node).name=”李刚刚的故事\0”`
在现实生活中，上面的故事显然是不符合常理的。现在，我们抛弃现实生活中的实际。我们世界上假设只有两个人。  
这两个人的衣装是不同的，我们显然可以根据这种特征去定位一个人。但是人数增多到一个量级后我们就不能根据人的衣装甚至名字来找到他。  

## `(chapter+1)->(node+1).name=”送餐员的需要\0”`
我不禁在想，送餐员需要一种可以定位到人的信息，这种信息是什么呢？我们能否根据这种信息具有的特性来反馈给送餐员呢？  
我总结了一下这类信息，发现他们具有以下两个性质：   
-	确定性
-	唯一性

## `(chapter+1)->(node+2).name=”确定唯一的信息\0”	4`
这种信息到底是什么？我们在日常生活中来确定一个人只需要一个具体的位置和一个可以联系到你的电话号码。当然，我们身上所有的信息也可以来确定一个人（每个人都是独一无二的）。那我们为什么不把自己所有的信息告诉送餐员呢？显然他太大了！可能你自己都不知道你自己的所有信息。

# `chapter[2].name=”程序中的地址\0”`
想一想在编写计算机程序中为了找到一个地址，你会怎么做。

## `(chapter+2)->(node).name=”取地址\&\0”`
当然在计算机中我们为了修改一个数组中的数据将数组的全部元素作为一个参数去传入函数中是不可以接受的（他太缓慢了），那为什么之前我们写程序中传入了数组也没有感觉程序运行的缓慢。有两个原因：  
-	数组长度太小（100以内？）
-	在c语言中，数组名就是地址（没想到吧？）  
  
于是我们需要传入数组的地址，还好在许多高级语言中把“&”规定为取地址符，使用它他可以获取到任意一个变量在计算机中的位置。 

## `(chapter+2)->(node+1).name=”间接访问\*\0”`
我们拿到一个地址后，这是一个整数型的数字，他是某一块内存的编号，通过“*”可以针对这个编号去访问计算机内存上的内容。也就是说我们想传递一个超大数组的时候，并不需要将这个超大元素传过去，只需要把这个超大数组的首地址地址传入，在函数内需要访问时，我们再去访问他即可。

# `chapter[3].name=”指针模型\0”`
以编程者的方式看待程序中的变量  

## `(chapter+3)->(node).name=”思维转变\0”`
以前在学习这部分知识的时候，教科书上引导我们使用计算机的方式去理解指针，我们才会越来越糊涂，现在我们需要转变一下思维，以编程者的方式去重新看待指针。  

***我曾不止一次说过思维的转变，才是化繁为简的最终奥义！***  


## `(chapter+3)->(node+1).name=”简单模型\0”`
当我们尝试声明一个变量，现在这个变量在我们的视角里是这样的。
 ![简单模型](http://t.cn/E4zPNwI)

实线表示我们知道的内容，虚线代表实际上存在，但是我们不知道的内容，因为这个内存位置是计算机在内存中寻找到一块合适的位置，申请出来的。也就是当我们在程序中int a=5的时候，我们现在只知道a的值是5，对于其他内容我们是一无所知的。但是当我们想要去找到a的地址，我们想要去知道a的上下内存空间存储了什么内容的时候，我们需要使用在第三章我们提到的取地址符进行访问

## `(chapter+3)->(node+2).name=”一级指针模型\0”`
人为的去开辟一个空间来存储这个地址，那我们说这个空间就是指针，或者说一级指针模型，那在程序中表示我在前面给回给出来，为了方便区分部分我把颜色分开了。如果●代表a这个变量，那么他的外部红色的线条框代表&a。指针模型与他类似，我们用*a代表●，而外部红色是a。@他就像把之前模型反过来表示的一样。
 ![一级指针模型](https://t.cn/E4zPHXV)


 
## `(chapter+3)->(node+3).name=”二级多级指针模型\0”`
仿照上述变换，加一层指针的话，应该变成如下图所示：
 ![二级多级指针模型](https://t.cn/E4zPmXR)


此后无论多少级的指针均可以用这个模型来表示了。我常常把他比作大娃娃里面的小娃娃那个玩具一样一层一层的，我把指针模型的界面给大家展示出来了，其实我们把图像变成立体图应该也可以想得通。  

# `chapter[4].name=”换不过来的交换\0”`
这块我们会使用指针进行一些程序开发，我们像大多数人一样以swap（交换函数）为例子，开始我们的实战。  

## `(chapter+4)->(node).name=”最简单的交换\0”`
下面是一个最简单的交换例子1，因为不涉及到参数，我们只需要显示的去改变a和b的值即可。  

```c
void swap_demo()
{
    int a = 1, b = 2;
    int *aptr = &a, *bptr = &b;
    printf("value of a is %d,adress of a is %p\n", a, aptr);
    printf("value of b is %d,adress of b is %p\n", b, bptr);
    *aptr = 2;
    *bptr = 1; 
    printf("value of a is %d,adress of a is %p\n", a, aptr);
    printf("value of b is %d,adress of b is %p\n", b, bptr);
    return;
}
```  


这只是个热身，我们先不要着急继续，我们先思考一下，我们到底在让什么进行交换，是值，地址还是指针的地址，很多同学因为这个不清楚而导致无法写出来程序。  

对了，我们只是在交换两个变量的值，所以不按照我的写法你自己是不是也可以写出来一个简单的例子呢？  

## `(chapter+4)->(node+1).name=”函数的交换\0”`
试想一下这种情况，你要把两个变量在函数里进行交换，但是函数中传入的参数并不会让你完成这种交换，因为作为参数在函数结束时是不会发生改变的，c语言中为了解决这个问题提供的地址传入的方式，设想一下，我们传入了两个数的地址，而在函数体内是对他们地址所指向的值进行交换，这样既不会改变参数中的值又可以完成地址的交换了。  

下面我给出函数：  


```c
void swap_function(int *p1, int *p2)
{
  int c = *p1;
  *p1 = *p2;
  *p2 = c;
  return;
}
```

## `(chapter+4)->(node+2).name=”地址的交换\0”`
那我们既然通过传入地址参数改变了值，当我们想改变地址的时候应该传入什么呢？因为函数执行结束不会改变参数的值，那我们只好传入地址的地址，这样可能会有点难以理解，我们我们可以应用我刚刚提出来的模型去想下，我们传入的地址只是为了改变我们要改变的地址，取道我们要改变的地址来改变。这样可能一时难以理解，多画图相信你可以熟练掌握。我这里给出地址交换的源码。看看你和我想的是否一样。  

```c

void swap_adress_function(int **a, int **b)
{
  int *c = *a;
  *a = *b;
  *b = c;
  return;
}
```


# `chapter[5].name=”字符指针\0”`

## `(chapter+5)->(node).name=”详解\0”`
我们经常用到char* a=“ABC\0”那么这句好话到底是什么意思呢？以这个为例子
我们要输出ABC怎么实现。我们想取道B字母怎么实现。利用指针模型，我们知道a是一个指针变量，他存储着A字符的地址，他的下一个地址存放的是B，同理他的下下个地址单元存放的是C。c语言怎么去实现分配单元空间呢？‘\0‘表示一个字符串的结束，无论你申请多大的空间，只要字符串中出现了‘\0‘这个指针就停止了，这也就是为什么你申请一个100长度的数组，调用strlen函数时他总是可以传给你这个字符串的长度而不是100。同时，我们想要在键盘上输入一个字符串没有办法输入‘\0‘怎么办？在c语言中，我们要输入字符串用’%s’来作为格式化输入，程序会为我们自动补充‘\0‘。
## `(chapter+5)->(node+1).name=”寻找大兵雷恩\0”`

我们想要实现在一个支付床str里面找到char find这个字符该怎么办呢？你可以先思考一下，我给出我的解决方案。

他非常简单，仅仅使用res来保存现在字符串的未知，当遍历完字符串依然没有我们需要的字符时，我们将-1返回即可。

```c
int find_char(char *str, char find)
{
  int res = -1;//计数器
  while (str++)
  {
++res;
    if ((*str) == find)//如果找到
    {
      return res;
    }
    if ((*str) == '\0')//退出条件
    {
      return -1;
    }
  }
  return -404;//其他情况
}
```
# `chapter[6].name=”其他案例\0”`
到这里，你的指针知识已经很强大了，我下面提供了几个练习案例，你可以先尝试自己编写，在于我的程序对应看一看你的进步吧！

```c
-	前序创建和遍历二叉树
#define TREESTR "abd--e--cf--g--\0"

typedef struct node
{
  struct node *left;
  struct node *right;
  char data;
} node, *nodeptr;

typedef struct bitree
{
  // int num;
  nodeptr root;
} bitree, *bitreeptr;
/**
 * @desc 为bt树bt树封装了一棵树的root节点
 * - malloc创建bt
 * @param (bitree **) bt 树根
 * @return void
 */
void creat_bitree_head(bitreeptr btp);
/**
 * @desc 为bt树创建node节点
 * - 为bt树创建node节点
 * @param (bitree) bt 树根
 * @param (node *) np 树根或者子树根或者叶子节点
 * @return void
 */
void creat_bitree_node(bitree bt, nodeptr *np, char **elem);
/**
 * @desc 通过根节点遍历二叉树！
 * - 通过根节点遍历二叉树！
 * @param (node) root 某棵树的根节点
 * @return void [打印前序遍历的二叉树，原则上与构造字符串相同]
 */
void print_bitree(node root);
// 模拟main环境
void bitree_main();

void bitree_main()
{
  bitree bt;
  char *str = TREESTR;
  creat_bitree_head(&bt);
  creat_bitree_node(bt, &((&bt)->root), &str);
  print_bitree(*((&bt)->root));
}

void creat_bitree_head(bitreeptr btp)
{
  // (*btp) = (bitreeptr)malloc(sizeof(bitree));
  // if (!*btp)
  //   exit(-500);
  // btp->num = 1;
  btp->root = (nodeptr)malloc(sizeof(node));
  if (!btp->root)
    exit(-500);
  return;
}

void creat_bitree_node(bitree bt, nodeptr *np, char **elem)
{
  char cur = *((*elem)++);
  if (cur == '-')
  {
    (*np) = NULL;
    return;
  }
  (*np)->data = cur;
  (*np)->left = (nodeptr)malloc(sizeof(node));
  if (!(*np)->left)
    exit(-500);

  (*np)->right = (nodeptr)malloc(sizeof(node));
  if (!(*np)->right)
    exit(-500);

  creat_bitree_node(bt, &((*np)->left), elem);
  creat_bitree_node(bt, &((*np)->right), elem);

  return;
}

void print_bitree(node n)
{
  printf("%c", n.data);
  if (n.left)
    print_bitree(*(n.left));
  else
    printf("-");
  if (n.right)
    print_bitree(*(n.right));
  else
    printf("-");
}
#	还记得Python类中的那个self吗？我们试着来实现一下！
typedef struct People{
  char * name;
  int age;
}People,*_People;

// 模拟main环境
void object_main();
/**
 * @desc set方法
 * - 实现 对 参数self结构体赋值
 * @param (const _People) self _People的地址 不可以在函数内发生改变
 * @param (char*) name 姓名的字符串
 * @return (void) [打印地址，不返回参数]
 */
void setName(const _People self,char * name);
/**
 * @desc set方法
 * - 实现 对 参数self结构体赋值
 * @param (const _People) self _People的地址 不可以在函数内发生改变
 * @param (int) age 年龄
 * @return (void) [打印地址，不返回参数]
 */
void setAge(const _People self,int age);
/**
 * @desc get方法
 * - 实现 对 参数self结构体赋值
 * @param (const _People) self _People的地址 不可以在函数内发生改变
 * @return (char*) name 姓名的字符串
 */
char * getName(const _People self);
/**
 * @desc set方法
 * - 实现 对 参数self结构体赋值
 * @param (const _People) self _People的地址 不可以在函数内发生改变
 * @return (int) age 年龄
 */
int getAge(const _People self);

void object_main()
{
  People son9wx;
  setName(&son9wx,"songwx\0");
  setAge(&son9wx,18);
  printf("user name is %s\n",getName(&son9wx));
  printf("user old is %d\n",getAge(&son9wx));
  return;
}

void setName(_People self,char * name)
{
  self->name = name;
  return;
}

void setAge(_People self,int age)
{
  self->age = age;
  return;
}

char * getName(_People self)
{
  return self->name;
}

int getAge(_People self)
{
  return self->age;
}
```



# `chapter[7].name=”后记\0”`
我在上数据结构课程的时候老师经常与我们互动，他对我很是困惑，虽然我可以在课堂上给出正确的答案，但是我的解题过程往往惨不忍睹，当我意识到这一点的时候，我开始改变，看是注重过程，开始注重变化，这让我安静了不少，同时再回头看自己写的程序的时候，确实发现很多不好的习惯，让我无法准确找到自己的错误，经常拆了东墙补西墙。但是改正的过程很痛苦，良好的习惯在一开始就形成的话会让你事半功倍，这篇文章虽然知识不多，但是能带给你很多良好的习惯。在指针中粗心大意往往会带来不可估计的后果，野指针，访问NULL都会让你的程序出现错误，希望你在编写时先想好再去写，你需要一份完整的图示或者说明去实现你的程序，这是一种优质的习惯，也是一个优质程序员的素养。

最后附上关于这本书目录的编程实现：


```c
typedef struct Node
{
    char * name;
} Node;

typedef struct Chapter
{
    char * name;
    Node * node;
} Chapter;

int init()
{
    int i ,j;
    Chapter * chapter = (Chapter*)malloc(sizeof(Chapter)*10); // 初始化章节
    for(i = 0; i<10; i++)
        (chapter+i)->node = (Node*)malloc(sizeof(Node)*10); // 初始化章节对应的小节

    for(j = 0; j<10; j++)
        for(i = 0; i<10; i++)
            chapter[j].node[i].name = (char*)malloc(sizeof(char)*15); // 初始化小节name

    for(i = 0; i<10; i++)
        chapter[i].name =  (char*)malloc(sizeof(char)*15); // 初始化章节name

    chapter[1].name = "第一章\0"; 
    chapter+1->node[1].name = "第一节\0"; 

    printf("现在是 %s,%s\n",chapter[1].name,(chapter+1)->node[1].name);

    return 0;
}
```
