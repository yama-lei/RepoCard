# RepoCard
A card component for github repository. 

一个github仓库卡片组件，可用于博客等处。

**The origin 出处: https://theme-plume.vuejs.press/guide/components/github-repo-card/**

## OutLook 外观

<img src="https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/20250306190758.png"/>

<img src="https://yamapicgo.oss-cn-nanjing.aliyuncs.com/picgoImage/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-06%20191134.png"/>

You will find it easy to modify the style in the vue component.

组件内容很简单，样式可以轻松更改。

## Usage使用方法

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





