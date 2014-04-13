### 5.4 在类上使用ExtractBy

对于某一类需求，我们会发现，前面提到的注解模式是无法满足的：一个页面有多条要抽取的元素，因为在之前的模式，我们一个页面是只有一条结果。例如在“QQ美食”的列表页面[http://meishi.qq.com/beijing/c/all](http://meishi.qq.com/beijing/c/all)，我想要抽取所有商户名和优惠信息，该怎么办呢？

在类上使用`@ExtractBy`注解可以解决这个问题。

在类上使用这个注解的意思很简单：使用这个结果抽取一个区域，让这块区域对应一个结果。

```java
@TargetUrl("http://meishi.qq.com/beijing/c/all[\\-p2]*")
@ExtractBy(value = "//ul[@id=\"promos_list2\"]/li",multi = true)
public class QQMeishi {

    @ExtractBy("//div[@class=info]/a[@class=title]/h4/text()")
    private String shopName;

    @ExtractBy("//div[@class=info]/a[@class=title]/text()")
    private String promo;

    public static void main(String[] args) {
        OOSpider.create(Site.me(), new ConsolePageModelPipeline(), QQMeishi.class).addUrl("http://meishi.qq.com/beijing/c/all").thread(4).run();
    }

}
```