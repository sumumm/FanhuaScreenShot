# 友链自动截图

**【参考项目】**

<table style="border:2px solid #000000;">
    <tr style="border:2px solid #000000;">
        <td align="center" style="border:2px solid #000000;">参考项目</td>
        <td align="center" style="border:2px solid #000000;">项目地址</td>
    </tr>
    <tr style="border:2px solid #000000;">
        <td align="left" style="border:2px solid #000000;">ChenYFan/ScreenShot</td>
        <td align="left"><a href="https://github.com/ChenYFan/ScreenShot" target="_blank">https://github.com/ChenYFan/ScreenShot</td>
    </tr>
    <tr style="border:2px solid #000000;">
        <td align="left" style="border:2px solid #000000;">Akilarlxh/ScreenShot</td>
        <td align="left" style="border:2px solid #000000;"><a href="https://github.com/Akilarlxh/ScreenShot" target="_blank">https://github.com/Akilarlxh/ScreenShot</td>
    </tr>
</table>

**【步骤】**

向<https://github.com/[GithubUserName]/[ScreenShot-RepositoryName]/blob/master/.github/workflows/GetScreenShot.yml>按照格式提交PR，**禁止更改大小参数**

添加一行

```
curl https://image.thum.io/get/width/400/crop/800/allowJPG/wait/20/noanimate/https://<YourDomain>/ -o <YourDoamin>.jpg
```

**【说明】**

截图默认大小 400\*266 默认宽度为 width 后面的像素值。crop的计算方法有些不同，虽然官方文档说是高度像素，但是实际测试发现应该是height=width*(crop/1200)。具体文档可以访问 <a href="https://image.thum.io" target="_blank">https://image.thum.io</a> 查看。

可在<https://cdn.jsdelivr.net/gh/[GithubUserName]/[ScreenShot-RepositoryName]@gh-pages/>看到预览图

**【引用格式】**

```html
https://cdn.jsdelivr.net/gh/[GithubUserName]/[ScreenShot-RepositoryName]@gh-pages/[friend_link].jpg

<!-- 例如 -->
https://cdn.jsdelivr.net/gh/qidaink/FanhuaScreenShot@gh-pages/qidaink.gitee.io.jpg
```

**【注意】**

可能不适配 pjax：本来是直接txt文件批量下载的，但是GithubAction的curl不能识别大括号下载方式

