# Sphero RVR
![](/img/rvr_bar.jpeg)

!!! 提醒
    建议使用 APP 把固件升级到最新

## 介绍
RVR 是 Sphero 出品的一款教育机器人，内置多种传感器并支持丰富的硬件改装。此扩展可以实时控制通过蓝牙连接的 RVR。


## Demo
<video width=80% src="/video/rvr345345.mp4" controls="controls"></video>

## 进阶
### API
使用 **广播** 积木调用 Python API: [Sphero Edu API](https://spherov2.readthedocs.io/en/latest/sphero_edu.html)

## bug 记录
只要 `import bleak` 就会出现这个问题.(lego mario也是)

windows10 的某些版本（[32bit 19041-SP0](https://item.m.jd.com/product/10026933866200.html?wxa_abtest=o&utm_source=iosapp&utm_medium=appshare&utm_campaign=t_335139774&utm_term=Wxfriends&ad_od=share&utm_user=plusmember&gx=RnFlx2ALOzTdndRJ-tE-G6S52g)）认为该插件存在安全问题，导致adapter退出，参考

*  [How do I setup configuration when I use command line to build C#/.NET?
](https://stackoverflow.com/questions/6469513/how-do-i-setup-configuration-when-i-use-command-line-to-build-c-net)
*  [loadFromRemoteSources](https://stackoverflow.com/questions/17615769/running-an-ironpython-script-from-python-sandbox-loadfromremotesources)

造成bug的原因可能是依赖库造成的（因为调用系统蓝牙？）

ps: 4.9.0 或许可用。


<!--
## test block
<script src="https://scratchblocks.github.io/js/scratchblocks-v3.4-min.js"></script>
<script src="https://scratchblocks.github.io/js/translations-all-v3.4.js"></script>

<pre class="blocks">
当 ⚑ 被点击
全部擦除
重复执行 
  落笔
  如果 <<按下鼠标?> 与 <碰到 [mouse-pointer v] ?>> 那么 
    换成 [button v] 造型
  否则 
    将 (x 坐标) 加入 [list v]
  end
  移动 (foo) 步
  左转 ↺ (29) 度
end
</pre>

<script>
scratchblocks.renderMatching('pre.blocks', {
  style:     'scratch3',   // Optional, defaults to 'scratch2'.
  languages: ["zh_cn"], // Optional, defaults to ['en'].
});
</script>
-->