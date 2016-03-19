# 基础Superblock

该部分介绍ZumDown默认支持的Superblock。一款符合标准的ZumDown渲染器应当支持这些类型的Superblock，但在一些使用场合，您的权限可能会被管理员配置为受限，这种情况下便会有一些功能无法使用。本文档中也会注明这些可能需要管理员赋予您权限才能使用的类型所需要的权限。

## 代码

**类型名称：** `code`

用于插入代码，自带语法高亮。

示例：

```code:zumdown
    ```code:python
    def foo():
        return bar()
    ```
```

**显示效果：**

```code:python
def foo():
    return bar()
```

```alert:info
该类型的Superblock最好不要放在嵌套结构中，否则缩进可能会混乱。
```

## 面板

**类型名称：** `panel`

```alert:info
**权限需求：** ZumDown.permission.perm.panel
```

用于创建一个带标题栏的框状物，标题栏的颜色可以选择。

该类型拥有一个可选参数，指定标题栏的颜色，它可以为以下几种：

* default
* success
* info
* warning
* danger

如果不指定该参数，则默认为default。

该块的正文第一行是特殊的，它用来指定该面板的标题。该块正文内支持书写ZumDown代码，并且可以嵌套Superblock。

示例：

```code:zumdown
    ```panel
    标题
    内容
    ```

    ```panel:success
    颜色类型为success的面板
    内容
    ```

    ```panel:info
    颜色类型为info的面板
    内容
    ```

    ```panel:warning
    颜色类型为warning的面板
    内容
    ```

    ```panel:danger
    颜色类型为danger的面板
    内容
    ```
    
```

**显示效果：**

```panel
标题
内容
```

```panel:success
颜色类型为success的面板
内容
```

```panel:info
颜色类型为info的面板
内容
```

```panel:warning
颜色类型为warning的面板
内容
```

```panel:danger
颜色类型为danger的面板
内容
```


## 警示条

**类型名称：** `alert`

```alert:info
**权限需求：** ZumDown.permission.perm.alert
```

用于创建一个小型警告条，颜色风格可选。

该类型拥有一个可选参数，指定颜色风格，它可以为以下几种：

* success
* info
* warning
* danger

如果不指定该参数，则默认为info。

该块正文内支持书写ZumDown代码，并且可以嵌套Superblock。

示例：

```code:zumdown
    ```alert
    标题
    内容
    ```

    ```alert:success
    颜色类型为success的面板
    内容
    ```

    ```alert:info
    颜色类型为info的面板
    内容
    ```

    ```alert:warning
    颜色类型为warning的面板
    内容
    ```

    ```alert:danger
    颜色类型为danger的面板
    内容
    ```
    
```

**显示效果：**

```alert
标题
内容
```

```alert:success
颜色类型为success的面板
内容
```

```alert:info
颜色类型为info的面板
内容
```

```alert:warning
颜色类型为warning的面板
内容
```

```alert:danger
颜色类型为danger的面板
内容
```

## 注释

**类型名称：** `comment`

用于插入注释，注释不会被渲染。

## 直接插入HTML

**类型名称：** `rawhtml`

```alert:warning
**权限需求：** ZumDown.permission.perm.html
**大部分网站的管理员不会允许您使用这种功能，因为它可能给网站带来XSS攻击等风险***
```

## 对齐方式

**类型名称：** `align`

用于改变内部文本的对齐方式。

该类型拥有一个可选参数，指定文本对齐方式，它可以为以下几种：

* left
* right
* center
* justify
* nowarp

如果不指定该参数，则默认为left。

该块正文内支持书写ZumDown代码，并且可以嵌套Superblock。

示例：

```code:zumdown

    ```align:left
    左对齐
    ```

    ```align:right
    右对齐
    ```

    ```align:center
    居中
    ```

    ```align:justify
    两端对齐
    ```

    ```align:nowarp
    不换行
    ```

```

**显示效果：**

    ```align:left
    左对齐
    ```

    ```align:right
    右对齐
    ```

    ```align:center
    居中
    ```

    ```align:justify
    两端对齐
    ```

    ```align:nowarp
    不换行
    ```

