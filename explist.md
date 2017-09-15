java demo:
public static void main(String[] args) throws Exception {
    Jsoup.connect("http://music.163.com/playlist?id=317113395")
            .header("Referer", "http://music.163.com/")
            .header("Host", "music.163.com").get().select("ul[class=f-hide] a")
            .stream().map(w-> w.text() + "-->" + w.attr("href"))
            .forEach(System.out::println);
}

类似上面的 只是一个java抓取的事例。

我个人只是习惯用C++ 和 Go 来编程，对于id的累加可以用一个for 循环来执行。前期是要做一个框架出来的，后面再进行累加。

个人推荐Qt作app的界面设计，网页形式的播放器，建议使用插件方式，qt 的demo代码可以联系本人。 以上只是个人建议。

                                                                                                turkeyzhu

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
