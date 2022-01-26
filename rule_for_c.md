# C语言编程规则
## 通用规则
* 源文件，头文件命名统一采用小写单词+蛇形命名法，具体如下
  ```c
  component_handler.c
  websocket_data_parser.h
  ```
* 优秀的代码是自注释的，如果命名或者逻辑能不言而喻，就无需对代码加上注释
* 头文件无特殊需要不要嵌套包含其他头文件，以免引起依赖错误
* 头文件是对外的接口，源文件中无需外引的函数，不用在头文件中声明，同时需要设定其属性为static
* 行与行之间，tab的缩进统一采用4个空格
* return语句要和前一句语句空出一行，除非return只有一行，例如在循环体中
## 变量规则
* 命名  
  通用变量命名采用小驼峰+蛇形命名法：首字母小写，单词间加下划线，具体如下  
  ```c
  client_Info，current_Data
  ```
  ### 前缀
  全局变量：g_  常量：c_  
  静态变量：s_  
  指针变量：p_  
  临时，中间变量：t_  
  数组：A_  
  结构体：S_  
  枚举：E_  
  联合体：U_  
  ```c
  gSA_Unit_Member
  ```
## 函数规则
* 命名  
  函数命名采用大驼峰+蛇形命名法：首字母大写，单词间加下划线，具体如下
  ```c
  Client_Data_Parse(int a, int b)
  ```
## 循环体规则
### if-else
* if后的条件判断需要加空格
  ```c
  if (true)
  ```
* if-else循环体要用大括号包围，且格式如下
  ```c
  if (true)
  {
      循环体1   
  }
  else
  {
      循环体2
  }
  ```
### while
* while后的条件判断需要加空格
  ```c
  while (true)
  ```
* while循环体要用大括号包围，且格式如下
  ```c
  while (true)
  {
      循环体
  }
  ```
* do-while也采用类似规则
### switch
* switch后的事件选项需要加空格
  ```c
  switch (ID)
  ```
* switch中的选项，除非逻辑需求，否则都要加上break和default
  ```c
  switch (ID)
  {
      case 1:
          printf("Hello1!");   
          break;
      case 2:
          printf("Hello2!");
          break;
      default:
          printf("default");
          break;
  }
  ```
