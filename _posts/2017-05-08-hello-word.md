---
layout:     post
title:      Hello Word!
date:       2017/5/10 18:52:38 
author:     Tanner Hu
summary:    Blog测试
categories: jekyll
thumbnail:  heart
tags:
 - Hello
 - Word
---
# 标题1 #
测试下博文功能~
# 标题2 #
测试下博文功能~
### 标题3 ###
测试下博文功能~
#### 标题4 ####
测试下博文功能~

# CODE #


`bundle exece jekyll serve`

# 代码 高亮ruby #

{% highlight ruby %}
class Awesome < ActiveRecord::Base
  include EvenMoreAwesome

  validates_presence_of :something
  validates :email, email_format: true

  def initialize(email, name = nil)
    self.email = email
    self.name = name
  end
end
{% endhighlight %}

# 代码块 薄荷主题 #

```html
<!DOCTYPE html>
<title>Title</title>

<style>body {width: 500px;}</style>

<script type="application/javascript">
  function $init() {return true;}
</script>

<body>
  <p checked class="title" id='title'>Title</p>
  <!-- here goes the rest of the page -->
</body>

```

# 列表 #

  * Apples
  * Oranges
  * Potatoes
  * Milk

  1. Mow the lawn
  2. Feed the dog
  3. Dance



# 图片 #

![Thumper](http://www.siweiw.com/Upload/sy/2014061602/dwtp%20%28120%29.jpg)

# 引导 #

`>`

>简单快速的引导符号

# 数学符号 #

`$$ E = m \cdot c^2 $$` 生成 $$ E = m \cdot c^2 $$

更多的


$$ \zeta(s) = \frac{1}{\Gamma(s)} \int \limits_0^\infty x^{s-1} \sum_{n=1}^\infty e^{-nx} \mathrm{d}x = \frac{1}{\Gamma(s)} \int \limits_0^\infty \frac{x^{s-1}}{e^x - 1} \mathrm{d}x $$
