# Superblock嵌套

Superblock的嵌套是比较特殊的功能，使用起来会稍微有点复杂。在嵌套结构的Superblock中，应当使用`(sbl-N)`这样格式的标签替代原本的三重\`，其中N是层级，依次为0,1,2,3,4,5,6,ex,ph。

直接上示例代码吧：

### 示例代码

```code:zumdown

    (sbl-0)panel:warning
        这是第一层标题
        
        (sbl-1)panel:info
            这是第二层标题

            (sbl-2)panel:danger
                这是第三层标题
                
                这是第三层内容第一行
                这是第三层内容第二行

                >这是第三层内容里的块引用

                (sbl-3)panel
                    这是第四层标题

                    (sbl-4)panel:success
                        这是第五层标题

                        (sbl-5)panel:primary
                            这是第六层标题

                            (sbl-6)panel:danger
                                这是第七层标题

                                (sbl-ex)panel:info
                                    这是第八层标题

                                    已经第八层了哦~

                                    (sbl-ph)panel:primary
                                        这是第⑨层标题

                                        啊已经九层了还不知足吗？
                                    (sbl-ph)
                                (sbl-ex)
                            (sbl-6)
                        (sbl-5)
                    (sbl-4)
                (sbl-3)
            (sbl-2)
            
            # 这是第二层内容里的大标题
            ***
            上面好像有一条分割线
            * 无序列表项1
            * 无序列表项2
            * 无序列表项3
        (sbl-1)
        
        诶，到最外面一层了~
        ## 这是一个二级标题
    (sbl-0)

```

### 显示效果

(sbl-0)panel:warning
    这是第一层标题
    
    (sbl-1)panel:info
        这是第二层标题

        (sbl-2)panel:danger
            这是第三层标题
            
            这是第三层内容第一行
            这是第三层内容第二行

            >这是第三层内容里的块引用

            (sbl-3)panel
                这是第四层标题

                (sbl-4)panel:success
                    这是第五层标题

                    (sbl-5)panel:primary
                        这是第六层标题

                        (sbl-6)panel:danger
                            这是第七层标题

                            (sbl-ex)panel:info
                                这是第八层标题

                                已经第八层了哦~

                                (sbl-ph)panel:primary
                                    这是第⑨层标题

                                    啊已经九层了还不知足吗？
                                (sbl-ph)
                            (sbl-ex)
                        (sbl-6)
                    (sbl-5)
                (sbl-4)
            (sbl-3)
        (sbl-2)
        
        # 这是第二层内容里的大标题
        ***
        上面好像有一条分割线
        * 无序列表项1
        * 无序列表项2
        * 无序列表项3
    (sbl-1)
    
    诶，到最外面一层了~
    ## 这是一个二级标题
(sbl-0)

### 注意事项

```alert:info
建议书写嵌套结构的Superblock时规范使用缩进，这样不仅仅使得代码易读，也不容易出现渲染错误。
```

```alert:info
code类型的Superblock最好不要放在嵌套结构中，否则缩进可能会混乱。
```

```alert:warning
默认情况下渲染器允许九层嵌套，但如果在某些使用场合，可能渲染器会被配置成受限的嵌套层级数，可能会低于九层。
```