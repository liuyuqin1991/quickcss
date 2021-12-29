# quickcss
一个能提高开发效率的轻量级原子化CSS库

## 引入与使用

``` 
// 引入
npm i quickcss

// 全局使用
import 'quickcss/lib/main.css';
```

## 配置

### 1. 边距
控制元素内边距（padding）与外边距（margin）的功能类，m,mt,mr,mb,ml,mx,my（p,pt,pr,pb,pl,px,py）七个标准维度，在这七个维度上均定义了0-100以
<span style="color: #cf3b37">4px</span>
自增，以及100-500以
<span style="color: #cf3b37">10px</span>
自增的固定边距，
特殊边距除外。
#### 格式
* 维度-x

如下示例：
|   Class  | Properties  |
|  ----  | ----  |
| p-0  | padding:0 |
| m-0  | margin:0 |
| pt-4  | padding-top:4px |
| mb-4  | margin-bottom:4px |
| pl-92  | padding-left:92px |
| mr-60  | margin-right:60px |
| pb-470  | padding-bottom:470px |
| ml-230  | margin-left:230px |
| px-12  | padding-left:12px; padding-right:12px |
| my-20  | margin-top:20px; margin-bottom:20px |

### 2. 宽度与高度
用来设置元素宽度（width）和高度（height）的功能类，均定义了0-500px以
<b> 1px </b>
自增的固定宽度与高度，0-100%以
<b> 1% </b>
自增的的百分比长度与高度，特殊宽度高度（例如calc(),rem，vh等）除外。
#### 格式
* w(h)-x: 固定宽度（高度）
* w(h)--x: 百分比宽度（高度）

如下示例：
|   Class  | Properties  |
|  ----  | ----  |
| w-0  | width:0 |
| h-52  | height:52px |
| w-246  | width:246px |
| h-480  | height:480px |
| w--14  | width:14% |
| h-100  | height:100% |

### 3. 字体
用来控制元素字体大小（font-size）和粗细（font-weight）的功能类，定义了12-40以
<span style="color: #cf3b37">2px</span>
自增的固定字体大小和500-1500以
<span style="color: #cf3b37">100</span>
自增的固定字体粗细，特殊大小与粗细除外。

#### 格式
* fs-x: 字体大小
* fw-x: 字体粗细

如下示例：
|   Class  | Properties  |
|  ----  | ----  |
| fs-12  | font-size:12px |
| fw-500  | font-weight:500 |
| fs-18  | font-size:18px |
| fw-1200  | font-weight:1200 |

### 4. 布局
只用于控制flex布局类，仅包含对父容器的flex-direction，flex-wrap，justify-start，align-item这4个常用class以及对子容器flex:1这1个常用class，特殊flex布局除外。

#### 格式
* f-x： flex-direction与flex-wrap相关
* -x: justify-content相关
* --x: align-items相关

如下示例：
|   Class  | Properties  |
|  ----  | ----  |
| f-r  | flex-direction: row; |
| f-c  | flex-direction: column; |
| f-rr  | flex-direction: row-reverse; |
| f-cr  | flex-direction: column-reverse;|
| f-w  | flex-wrap: wrap; |
| f-nw  | flex-wrap: nowrap; |
| f-wr  | flex-wrap: wrap-reverse; |
| -s  | justify-content: flex-start; |
| -e  | justify-content: flex-end; |
| -c  | justify-content: center; |
| -sb  | justify-content: space-between; |
| -sa  | justify-content: space-around; |
| --s  | align-items: flex-start; |
| --e  | align-items: flex-end; |
| --c  | align-items: center; |
| --b  | align-items: baseline; |
| --st  | align-items: stretch; |
| f-1 | flex:1; |
| f-r -c --c  | flex-direction: row; justify-content: center; align-items: center;|
| f-c -sb --c  | flex-direction: row; justify-content: space-between; align-items: center;

### 5. 颜色
用于控制元素的文字颜色（color），背景颜色（background-color）和边框颜色（border-color）的功能类。这里颜色使用了qingcloud的portal-ui颜色库。

#### 格式
* c-x： 文本颜色
* bgc-x: 背景颜色
* bc-x: 边框颜色

<span style="color: #d9615f">
注：这里x为portal-ui色系值，通过在chrome中使用figma color for qingcloud portal插件，能够在figma网页版设计稿中显示颜色色值对应的portal-ui定义的颜色变量（只看显示的第一个变量），然后根据所对应的色系和色值来定x，例如，#324558对应的$neutral-15，色系为n（neutral），色值为15，那么x=n15
</span>

如下示例：

|   Class  | Properties  |
|  ----  | ----  |
| c-n8  |  color: $help2 |
| c-n15  |  color: $title3 |
| c-g11  |  color: $primary |
| c-g11  |  color: $primary |
| bc-n3  |  border-color: $border-color |
| bgc-n0  |  background-color: $white |

### 6. 边框
用于控制元素边框半径（border-radius）和边框厚度（border-width）的功能类，定义了1-10以
<span style="color: #cf3b37">1px</span>自增的边框半径和定义了1-10以<span style="color: #cf3b37">1px</span>自增的边框厚度。定义了边框半径为半圆的1个特殊边框半径和3个子portal常用特殊的边框样式。边框颜色见颜色类。

#### 格式
* br-x： 边框半径
* bw-x: 边框厚度
* b-x: 特殊边框 

如下示例：

|   Class  | Properties  |
|  ----  | ----  |
| br-1  |  border-radius: 1px |
| br-8  |  border-radius: 8px |
| bw-1  |  border-width: 1px; |
| bw-5  |  border-width: 5px; |
| 特殊边框半径 |   |
| br--50  |  border-radius: 50% |
| 特殊边框（normal） |   |
| b-n |  border: 1px solid $border-color; |
| 特殊边框（light-normal） |   |
| b-ln |  border: 1px solid $light-border-color |
| 特殊边框（primary） |   |
| b-p |  border: 1px solid $primary; |

### 7. 其他
用于控制其他方面的功能类，持续的更新中，也会直接全部在示例中介绍

|   Class  | Properties  |
|  ----  | ----  |
| cur-p  |  cursor: pointer; |
| cur-na  |  cursor: not-allowed; |
