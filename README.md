使用vue写的各种组件，适合放在博客等场景。

欢迎参观我的博客[博客主页 | Myblog](https://yama-lei.top/)

## 1. RepoCard

A card component for github repository. 

一个github仓库卡片组件，可用于博客等处。

**The origin 出处: https://theme-plume.vuejs.press/guide/components/github-repo-card/**

### OutLook 外观

<img src="https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/20250306190758.png"/>

<img src="https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-06%20191134.png"/>

You will find it easy to modify the style in the vue component.

组件内容很简单，样式可以轻松更改。

### Usage使用方法

props为`repo`，传入`user/repo`即可,如`yama-lei/RepoCard`;

```vue
<RepoCard repo="yama-lei/RepoCard"></RepoCard>
```

组件默认宽度为100%，如果想要一行放置多个，需要手动套一层样式：

```vue
<div style="display: grid;grid-template-columns:repeat(2,1fr);">
<RepoCard repo="aialgorithm/AiPy"></RepoCard>
<RepoCard repo="aialgorithm/AiPy"></RepoCard>
<RepoCard repo="aialgorithm/AiPy"></RepoCard>
<RepoCard repo="aialgorithm/AiPy"></RepoCard>
</div>
```



---

## 2. TimeLine 时间轴



#### OutLook外观

<img src="https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-08%20105728.png" style="height: 600px"/>

#### Usage使用

```vue

<TimeLinePage :stories="myStories"/>

<script setup>
   const myStories = [
       {
      imageSrc: '',
      title: '除夕随便写点',
      description: '烟花只在除夕晚上好看，因为不用担心扰民',
      link:'NewYearEve',
      time:'2025-1-28',
      comments:'comments',
      showComments:false,
      likesNum:1
      },   
      { 
      imageSrc: '',
      title: '寒假社会实践结束了',
      description: '其实我觉得这次社会实践更像是面向ai编程范式的实践',
      link:'SocialPractice',
      time:'2025-1-28',
      comments:'comments',
      showComments:false,
    	likesNum:1,
      },{
	      imageSrc: '',
      title: '程序设计OJ又没过',
      description: '很简单的题目，在机房死活过不去，回来重写一遍就过了。',
      link:'',
      time:'2025-3-7',
      comments:'comments',
      showComments:false,
      likesNum:1,
      }
    // Add more stories as needed
  ]
</script>
```

>   可以在故事中添加评论，样式类似于markdown中的引用；
>
>   如果link字段为空，那么不会有卡片中“阅读原文”按钮。

## 3. Paper 信纸



#### OutLook 外观

![](https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-08%20163622.png)

#### Usage 使用

````vue
<template>
<div v-for="(letter,index) in letters">
    <Paper
        :title="letter.title"
        :time="letter.time"
        :main="letter.main"
        :imgUrls="letter.imgUrls"
    />
</div>
</template>
<script setup>
const letters=[
{
    title: "湖南到南京 | 我走了18年",
    time: "2025-3-8",
    author: "雷业成",
    main: [
        "亲爱的XXX：",
        "展信佳！",
        "今天是我开学第一天，报道的事儿忙完以后人有够闲的。突然想起要写入党申请书，所以先写封信练练手！哈哈。本来买了几种信纸和信封，但我还是觉得就用南大的信纸写更有一种独特的蕴味。",
    ],
    imgUrls: ['https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/a79091a875a18ee70ee7919792fbd64.jpg',
                'https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/797a2429a7ade8af99f332c25d172a5.jpg',
                'https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/7a8758104f1743f8552e6280f852937.jpg'
    ]
}
]
</script>
````

