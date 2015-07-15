---
layout: post
title: SpringMVC 与 FreeMarker
category: 技术
comments: false
---


## 约定优于配置 & 注解 -> 配置Route

* 使用 @Controller 配置控制器, 使用 @RequestMapping("/some_path") 来配置控制器路径
* 使用 @RequestMapping(value = "action_path")来配置Action对应的路径



```java
@Controller
@RequestMapping("/summary")
public class SummaryController {

  @RequestMapping(value = "index", method = RequestMethod.GET)
  public ModelAndView index() {
        ModelAndView mav = new ModelAndView("index");
        return mav;
  }
}
/** 将index() 映射到/summary/index 下, 到FreeMarker根目录下寻找index.ftl渲染结果页面**/
```







