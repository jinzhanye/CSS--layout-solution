## <<深入理解z-index>>笔记
- 可选值  
  - z-index:auto
  - z-index:\<interger>
  - z-index:inherit
  
- 特性
  - 支持负值
  - 支持CSS3 animation动画
  
  ````
    @keyframes zIndex{
        0%{z-index:-1;}
        100%{z-index:51;}
    }
  ````
  - 在CSS2.1时代，需要和定位元素配合使用
  ![](https://ws3.sinaimg.cn/large/006tNbRwgy1fmqr962hubj30mm0ey79x.jpg)
  
- 如果定位元素没有z-index嵌套
    1. 后来居上的准则
    2. 哪个大，哪个在上面

- 如果定位元素有z-index嵌套
	1. 祖先优先原则
	 
- 触发创建层叠水平上下文的条件
	- 根元素（即html元素）
	- z-index 值不为 "auto"的 绝对/相对定位，
	- position: fixed
	- 一个 z-index 值不为 "auto"的 flex 项目 (flex item)，即：父元素 display: flex|inline-flex，
    - opacity 属性值小于 1 的元素

- overflow:auto 可能使 z-index 失效?

- 7阶层叠水平
>重要性：内容>布局>装饰
![](https://ws4.sinaimg.cn/large/006tNbRwgy1fmqsaj9b5ij30pn0gy42v.jpg)
