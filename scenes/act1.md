# act1

```
SceneSetup.act1();
```

(...300)

n: **这是这个人类的焦虑**

n: ***你*是这个焦虑**

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: 嘿！咱们咋又在这见面了？

`hong({eyes:"0_neutral"})`

n:  **你的职责是保护你的人类，让它远离*危险***

`bb({eyes:"look", mouth:"small_lock"})`

n:  **事实上，再次游玩这个游戏就是把它们再一次置于*危险*之中**

n: **快，警告它们！**

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听着，我们正处于危险之中，这个玩家......

[...正准备再一次折磨我们！](#act1_replay_torture)

[...不会找到另一个结局了！](#act1_replay_alternate)

[...会找到这款游戏隐晦的的叙事失调之处！](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: 它会让我们蜷成一个球大哭！
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: 它会让你惊恐发作，让我们砸毁你的手机！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: 它会*阻止*我们打那个派对主人！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: 它会逼我们打那个像悲情反派的派对主人！
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: 好吧，至少这次，我们可能不会再从屋顶跳下——
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b:  **它们会逼我们从屋顶上跳下去！。**
{{/if}}

`bb({body:"fear"});`

b:  **所有糟糕的事情都会降临在我们身上，之后我们就会——**

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 确实，这个故事的*基调*是一样的，但是每个章节都有两个可能发生的结局，而且所有的分支对话选择——

`bb({body:"fear"});`

b: 玩家会失望的。它们会关掉这个页面，删除我们的软件，然后我们就会——

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 淫秽的—什么......?

`bb({eyes:"normal"});`

b: 这整个故事都是在说你能*选择*和你的恐惧建立起良好的合作关系，

`bb({eyes:"normal_right"});`

b: 但是重新游玩这个游戏也只会给它们呈现一样的故事，不就是说你的*选择*毫无用处吗？

`bb({eyes:"narrow_eyebrow"});`

b: 这就暴露了这个游戏内容和机制的矛盾之处，

`bb({eyes:"fear"});`

b: 然后这个叙事宇宙的根基就分崩离析了，

`bb({body:"fear"});`

b: 然后我们就会——

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: **死**死死死死死死——

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h:  好吧，我们还是回到角色应有的表现里吧。

```
Game.clearText();
```

n4:（**让*你*的焦虑和*你*的恐惧瞎bb那些你早就知道的那些话去吧**）

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: 哈哈，我的狼回来了。真真真真是太好了啊。

`hong({eyes:"0_neutral"})`

n: **你的职责是保护你的人类，让它远离*伤害***

`bb({eyes:"look", mouth:"small_lock"})`

n: **事实上，这个三明治就在把它置于*危险*之中**

n: **快，警告它！**

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听着，我们正处于危险之中！就是......

`bb({body:"squeeze"})`

n4: （**让*你*的焦虑出来玩玩！挑个和*你*的恐惧告诉你最相近的内容！**）

(#act1_normal_choice)

# act1_normal_choice

[我们在一个人吃午餐，又一次！](#act1a_alone) `bb({body:"squeeze_talk"})`

[我们在吃饭的时候啥也没做！](#act1a_productive) `bb({body:"squeeze_talk"})`

[这个白面包对我们的身体不好！](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: 你难道不知道，孤独带来的早逝风险和每天抽15根香烟一样吗？-  

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (霍尔特-伦斯塔德 等，2010年，《公共科学图书馆·医学》)

`hong({eyes:"0_annoyed"})`

h: 呃，多谢你指出这句话的根据，但是——

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: 这意味着如果你不*立刻*和其它人出去玩的话你将会——

`bb({body:"panic"})`

b:  **死**死死死死死死死——————

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n:**你使用了*不被爱*的*恐惧***

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: 现在立马打开你的笔记本做点啥！

`hong({eyes:"0_annoyed"})`

h: 呃，我更不想把面包屑撒在我的键——

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 如果我们不对社会躯体做点贡献我们就成了社会寄生虫！

b: 社会躯体会去找社会医生开些药杀死那些社会寄生虫然后我们就会——

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: **死**死死死死死死死——————

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n:  **你使用了*变成一个坏人*的*恐惧***

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: 那些研究难道没有——

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 加工过的小麦会让我们的血糖激增所以它们会切掉我们的四肢然后我们就会——

`bb({body:"panic"})`

b: **死**死死死死死死死——————

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n:  **你使用了*被伤害*的*恐惧***

(#act1b)

# act1b

n:  **这简直太有效了！**

`bb({mouth:"smile", eyes:"smile"});`

b: 看到了吗，人类？！我是你忠实的看家狼！

`bb({body:"pride_talk"});`

b: 相信你的直觉！你的感觉总是可靠的！

`bb({body:"pride"});`

n:  **让你的人类的能量阈值降到零**

n:  **为了保护它们的生理+社会+道德需求，你可以使用：**

n: ***被伤害***的**恐惧** #harm#

n: ***不被爱***的**恐惧** #alone#

n: ***和变成一个坏人***的**恐惧** #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4:（**专业建议**：**选择那些会刺中你心底最深、最黑暗的恐惧的选项吧！~**）

h: ……

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: 呃，或许是时候查看我的手机消息了。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n:  **保护你的人类**

n:  **保护它们远离伤害：来自世界的。来自它人的。来自它们自己的。**

n:  **祝你好运**

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n:  **第一轮**：*战斗!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h:  唔，脸书动态说这周末有一个派对。

`bb({eyes:"uncertain"});`

b: 那些怪胎不是*每*周末都会举行派对吗？

`bb({eyes:"uncertain_right"});`

b: 它们在试图填满内心什么样的空虚？我就说，它们的内心一定是一团糟！

`hong({eyes:"surprise"});`

h: 而且，我被邀请了？

`bb({eyes:"fear", mouth:"normal"});`

b: 那么！

[答应它，不然我们会因为孤独而死去！](#act1c_loner)

[拒绝它，那里充斥着有毒的药物！](#act1c_drugs)

[无视它，我们只会让派对变得糟糕。](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: 一天十五根香烟，人类！十五根！
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: 没有人会出席我们的葬礼，它们会把我们的骨灰扔进大海，然后我们就会被鲸鱼吃掉，
{{/if}}

{{if !_.fifteencigs}}
b: 然后我们就会变成**鲸鱼的大便！！！**
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: 是的我们应该去那场派对！
{{/if}}

{{if _.parasite}}
b: 只是记得带上笔记本，这样我们就可以工作，不成为社会寄生虫了。
{{/if}}

{{if _.whitebread}}
b: 只要它们不提供**白面包**
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: **天哪**。如果这能让你闭嘴，好吧。

h: 我会答应的。

{{if _.whalepoop}}
b: 鲸鱼的大便，人类！鲸鱼的大便！
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: 或者更坏......**白面包**
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: 我们会嗑巨多毒品和白面包以至于它们无法把我们肥胖的尸体塞进焚化炉！
{{/if}}

{{if !_.whitebread}}
b: 我们会嗑太多药，连殡葬师都会震惊于我们的身体*早已经*进行过防腐工作了！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: 另外，我们不能去派对，我们得去工作，不然我们就会成为糟糕的社会寄生虫！
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h:  **天哪**，如果这能让你闭嘴，好吧。

h: 我会拒绝的。

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b:  我们能做的只是在一个角落里大哭，哭孤独和一天吸15根烟的致命程度相同。
{{/if}}

{{if _.parasite}}
b:  我们能在派对做的，就是担忧我们怎么样才能更加有生产力。
{{/if}}

{{if _.whitebread}}
b: 我们能做的，就是忧虑那些不健康的食物最终会怎样杀死我们。
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: 哇哦，那我可真想知道为什么。

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: 所以如果我们参加派对，就会让它们难受，但如果拒绝它们的邀请，我们也会让它们难受！

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b:  **我们能做的只是让别人难受，所以我们也应该感到难受**

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: 唉，如果这能让你闭嘴，好吧。

h: 我会无视那个邀请。

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: 算了，脸书太多消息了，我需要些更清净，不会让人焦虑的东西。     

`hong({eyes:"neutral"});`

h: 推特上有什么新鲜事吗？

`bb({eyes:"look"});`

[哦不，看那个糟糕的新闻！](#act1d_news)

[哦不，那是暗地里阴阳*我们*的推文吗？](#act1d_subtweet)

[嘿，一个猫猫喝牛奶的动图。](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: 天哪，这感觉就像是整个世界在燃烧，不是吗？

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: 感觉一切都已经注定了，所有事情都在死去，我们也会完蛋，我们还无能为力。

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ……

`bb({mouth:"smile", eyes:"smile"});`

b: 让我们转发这个推文吧！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 好的我会转发它的，只是求求你安静点！

`hong({mouth:"neutral", eyes:"annoyed"});`

h: 去你的，还不如看看snapchat。

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: 这是一个阴阳人的推特！一个悄咪咪指责别人的推特！

`hong({eyes:"annoyed"});`

h: 或许它不是呢？

`bb({eyes:"narrow", mouth:"small"});`

b: 但是如果它们在背后说我们坏话怎么办？

h: 它们没——

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: **在我们不知道的地方**

`hong({eyes:"sad", mouth:"sad"});`

h: 我——

`bb({eyes:"narrow", mouth:"small"});`

b: 但是*万一*

h: 闭——

`bb({eyes:"narrow_eyebrow"});`

b: *万一*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ……

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h:  呃，好，我还是看看snapchat吧。

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: 嘿，这真可爱，我想转发它，我觉得——

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: **猫不能消化牛奶所以我们是糟糕的从虐待动物里获取快感的人！！！**

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 呃，好，我还是看看snapchat吧。

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: 啊哈，昨晚的照片。所以*那*就是周末派对的样子。

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h:  噢，看上去人好多，或许对我现在的焦虑状态来说不怎么友好。

h: 或许我一开始不应该答应那个邀请？

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[改变我们的答复？像个傻瓜一样？](#act1e_yes_dontchange)

[改变我们的答复！那里人太多了！](#act1e_yes_changetono)

{{if _.subtweet}}
[是的，它们一定会私下里说我们的小话。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[等等，我们在转发那个推文前没有确认真相啊。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[你知道的，你已经选择了一个糟糕的态度去回应那个邀请。](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 它相信我们会去的，但是你现在要背弃它的信任？难道你想一个人孤零零死去吗？

{{if _.fifteencigs}}
b: **十五支，香烟。**
{{/if}}

{{if _.whalepoop}}
b: **鲸鱼的，大便。**

{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h:  闭上你的臭嘴吧，我会去的！

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 难道你没听说过那次踩踏事故吗？

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 2003年，罗德西亚岛的一家夜店着了火，结果惊慌使人们堵在紧急出口，最后活生生烧死了一百多人——

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: **你也想让那种事发生在我们身上吗**

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b:  **拒绝它拒绝它拒绝它拒绝它拒绝它拒绝它拒**


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭上你的臭嘴吧，我会改变我的答复！天哪！

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: 唔，看上去好好玩。

h: 或许我不该拒绝那个邀约？

`bb({mouth:"normal", eyes:"normal"});`

[改变我们的答复？像个傻瓜一样？！](#act1e_no_dontchange)

[改变我们的答复！可别一个人孤零零死掉！](#act1e_no_changetoyes)

{{if _.subtweet}}
[是的，它们绝对在私下里说我们的小话。](#act1e_ignore_subtweet)   
{{/if}}

{{if _.badnews}}
[等等，我们在转发那条推文前没有确认真相啊。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[你知道的，你已经选择了一个糟糕的态度去回应那个邀请。](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: 所有人都在指望我们！

b: ...让它自己呆着，并且让它那愉快的派对远离一个糟糕的、令人厌恶的 {{if _.whitebread}}大声咀嚼着白面包的{{/if}} 像你一样的怪胎......


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭上你的臭嘴吧，我不会去的！

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 长期的孤独会增加我们的皮质醇水平、接着就会增加得心血管疾病和中风的风险！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: **十五支、香烟。**
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭上你的臭嘴吧，我会改变我的答复！我会去的！天哪！

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 我们发过的那些黑历史果然找上头来了！

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: 我们会被骂、被抵制，还会被绑上绳子，被马在信息的高速公路上拖行！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 你为什么要这样子？！

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 我们在传播不实信息！我们正在摧毁人们对新闻自由的信任！

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b:  我们就是法西斯主义从民主主义的废墟中发展起来的元凶！ 

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: 你为什么要这样子？！

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b:你想拿蝴蝶酥当脊椎吗？！别驼着背看手机了！

```
bb({body:"meta"});
```

b: 你不也一样。

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 你为什么要这样子？！

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: 唔，看上去挺好玩的。

h: 或许我不该忽视那个邀请？

`bb({mouth:"normal", eyes:"normal"});`

[还是忽视吧。我们是扫兴鬼。](#act1e_ignore_continue)

[事实上，你应该答应它们。](#act1e_ignore_changetoyes)

[事实上，你应该拒绝它们。](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: 一直忽视下去或许有点粗鲁，不是吗？

`bb({eyes:"normal_right"});`

b: 可是其它人一直都忽视*我们*，所以

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: 所以就这样吧。

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: 你......让我去开心一下？

b: 好吧，毕竟孤独可是*能*杀了我们的。

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: 人太多了，人群是危险的。

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 无论如何，新的tinder消息来了。

`bb({eyes:"uncertain"})`

b: 什么？那个聊骚软件？

`hong({eyes:"annoyed"})`

h: 那不是什么聊骚软件，只不过是一种认识新朋友的——

`bb({eyes:"narrow"})`

b: 这就是聊骚软件。

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: 哇，配对成功了！它看起来很可爱！

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: 拜托不要再给我毁了这——

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: **危险危险危险危险危险危险——**

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[我们在被它人*使用*。](#act1f_used_by_others)

[我们只是在*使用*其它人](#act1f_using_others)

[**你的匹配对象是个连环杀手**](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: 随机聊骚或许能填补这里的洞，

b: 但是它们永远也不能填满，

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *这里*的洞

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 重点是，**我们会孤独地死去**

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: 你把别人的生殖器当宝可梦来收集吗？

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (宝可梦主题曲)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ 我想成为最 ^放荡的^-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ 就像从未有人-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ 大腿和 ' ^翘臀^, 性感的丰胸-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ 和亲爱的^阴茎^ 还有摇摇球-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ **变态宝可梦！抓到一个就-**

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 重点是，我们是操纵别人的变态。

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: 它们会把你困在井里，强制喂白面包给你，直到你胖的能够让它们剥下你的皮当大衣穿！
{{/if}}

{{if _.parasite}}
b: 它们会用番茄钟威胁你说： "**你个寄生虫早该多干点正事了**"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b:  它们会把你的血肉撕成五彩纸屑，把你的肠子扯成彩带，再把你的鲜血混进派对饮料里！
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: 这个邀请够**带劲**了吧？！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ……

(...500)

h: 我厌倦了这个游戏。

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"loneliness will kill us"... {{/if}}
{{if _.parasite}}"we're a society-parasite"... {{/if}}
{{if _.whitebread}}"don't eat that, it'll kill us"... {{/if}}
{{if _.subtweet}}"they're talking behind our back"... {{/if}}
{{if _.badnews}}"the world is burning"... {{/if}}
{{if _.hookuphole}}"we'll die alone"... {{/if}}
{{if _.serialkiller}}"they're a serial killer"... {{/if}}
{{if _.catmilk}}"cats can't digest milk"... {{/if}}
{{if _.pokemon}}a ^crappy^ parody song... {{/if}}

h: 我只是想好好过我的生活。

h: 我只是想远离所有这些......痛苦。

`bb({eyes:"look_sad"});`

b: 嘿......人类......

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: 会好起来的。

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: 作为你忠实的看家狼，我会永远关注着潜在的危险，尽我所能保护你的安全。

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: 我保证。

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: 最后一个软件，instagram。你看到了什么？

`hong({eyes:"sad"});`

h: 是......更多的派对照片，

`hong({mouth:"sad"});`

h: 所有人看起来都很开心。毫无担忧。毫无焦虑。

`hong({mouth:"anger"});`

h: 老天奶，为什么我不能像它们一样？为什么我连*正常*都做不到？

`bb({eyes:"normal_right"});`

b: 说到这周末的派对邀请。这是我的**最终**选择：

`bb({eyes:"normal"});`

[我们应该去。](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[我们不应该去。](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: 我们——

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^ *操* ^.*

`hong({body:"2_you"});`

h: **你**。

(...500)

b: 什

(...1500)

`bb({eyes:"wat_2"});`

b: 什么？

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: 我**会**去这场派对。

{{if _.act1g=="go"}}
h: **不是**因为你想让我去，而是因为*我*想去。
{{/if}}

{{if _.act1g=="dont"}}
h: 准确来讲，是**因为**你不想让我去。
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: 你**无法**掌控我。

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: 现在请你让我在这^该死的^平静中吃完这个美味的三明治。

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ……

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ……

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[**啊啊啊啊我们会死掉的！！**](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[**啊啊啊啊所有人都讨厌我们！！**](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[**啊啊啊啊我们真是烂透了！！**](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: **啊啊啊我们会死掉的啊啊啊啊啊啊啊！！**

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: **啊啊啊所有人都讨厌我们啊啊啊啊啊啊啊！！**

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b:  **啊啊啊我们烂透了啊啊啊啊啊啊啊！！**

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: **恭喜你**

(...500)

n:  **你成功地捍卫了你的人类的生理+社会+道德需求！**

n:  **为什么不是？看看它们多感激啊！**

(...500)

n: **既然它们的能量已经归零了，你可以直接控制它们的行动了！**

`bb({mouth:"smile", eyes:"normal"});`

n: **请选择你的结局杀招吧！**

`bb({mouth:"small_lock", eyes:"fear"});`

n: ***了结它们***

[{**战斗**: 给你的那台让人充满焦虑的手机些惩罚！}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{**战斗**: 蜷成一个球大哭吧！}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: 你的手机一直在恐吓你！

`bb({eyes:"anger"})`

b: Zuckerberg这群人正绑架你的精神健康，给那帮资本家们投钱呢！

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 惩罚你的手机！砸了它！杀了它！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: **杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它杀了它**——

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: 整个世界都充斥着危险！

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 像犰狳一样！蜷成一个球，保护自己！

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: **蜷起来大哭吧蜷起来大哭吧蜷起来大哭吧蜷起来大哭吧蜷起来大哭吧蜷起来大哭——**

(#act1j)

# act1j

`SceneSetup.act1_outro()`
