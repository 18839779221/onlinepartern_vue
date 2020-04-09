<template>
  <div class="main">
    <h2>{{content.active_event}}</h2>
<p class="title">发布时间:<em>{{content.active_time}}</em>&nbsp;&nbsp;地点:<em>{{content.active_location}}&nbsp;&nbsp;</em> 发布:<em>admin</em></p>
<hr/>
<p>&nbsp;&nbsp;&nbsp;&nbsp;{{ detail[content.id-1] }}</p>
  </div>

</template>

<script>
export default {
  name: "activityDetail",
  data(){
    return{
      content:{
        active_event:"aaaa",
        active_time:"",
        active_location:"",
        id:0,
      },
      detail:[
        "    按照约定时间到达地点后，会验证你的报名信息（微信或者APP报名成功后发的短信二维码），然后会给你一张小卡片以及三颗爱心小贴纸（男生是红色，女生是粉红色），让你填写卡片基本信息，同时现场会提供一些饮料畅饮和小部分零食。",
        "    清晨的第一缕阳光唤醒了你全新的一天，你独自走在上班的路上，身边车水马龙。傍晚亦或是深夜，结束了工作走在回家的路上，有些疲惫，却没有人给你一个温暖的拥抱。打开手机，通讯录里静静地躺着上百个联系人，而此时，你看到一个小小的幽默笑话却不知道分享给谁合适。约杯咖啡，百聊不如一见，Ta其实离你并不远。",
        "    有时候觉得老天真是不公平，作天作地还作死的妖孽都有人爱了，你那么努力善良又上进，却始终没有对象，是你不够好吗？是单身都瞎了眼吗？当然不是，只是和你无缝契合的那个人，还没来。感情的世界不是只靠喜欢就够了，相处舒服，性格默契，才是真正对的人啊！所以单身的你，请不要自我贬低，也不要信网络上说的“你不要急，你要等”。“等”是等不到真爱的~只有自己走出去，去遇见，去接触，才能知道他是不是你想要携手一生的人啊！",
        "    给追求幸福、美好生活的人提供一个平台，通过集体相亲活动，营造浓郁的浪漫氛围，让所有需要爱的人在轻松、浪漫、温馨种寻找到属于自己的幸福爱情。",
        "    7月1日，由江苏省省直机关工会主办，掌缘科技协办的“爱在初夏，缘聚南京”单身职工相亲联谊活动即将与南京单身男女见面，如果你还单着，那赶紧来报名吧！",
        "    中国这么大，单身这么多，我们却仍是一个人吃饭，睡觉，生活，在这个城市“孤单”吗?一场7日恋人の体验活动发起者，985、211、海归、硕博相亲平台六口茶社提供活动支持，也许你是普通上班族，设计师，金融师，也许你是大学生，老师，公务员，可在孤独面前，众生平等，找个人来一起完成一些有趣小任务吧，也许TA正在这里等着与你相遇。"
      ]
    }
  },
  methods:{
    //加载活动数据
    init(){
      this.content = JSON.parse(this.$route.query.content);
      console.log(JSON.parse(this.$route.query.content));
    }
  },
  mounted(){
    this.init();
  }
};

</script>

<style scoped>
.main{

  margin-left: 100px;
  margin-right: 100px;
}
.title{
  text-align: center;
}
h2{
  text-align: center;
}
</style>
