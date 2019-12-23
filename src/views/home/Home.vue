<template>
  <div class="home">
    <blogs :blogs="blogs"></blogs>
  </div>
</template>

<script>
// @ is an alias to /src
import Blogs from "./childComps/Blogs";

export default {
  name: "home",
  components: {
    Blogs
  },
  data() {
    return {
      blogs: []
    };
  },
  created() {
    // 进入主页请求文章数据列表并传到文章列表子组件中
    let blogTest = [
      {
        id: 1,
        title: "计算机考研，这样选学校才是正解",
        summary:
          "写了一篇《启舰：对计算机专业来说学历真的重要吗？》，一时间N多同学咨询自身情况要不要考研，眼看有点Hold不住，索性又出了一篇《启舰：计算机专业有必要考研吗？》，结果，又有同学说：“我是渣渣二本，想考985是不是难度太大？”“大城市竞争力是不是很大，我考研是不是应该考偏僻点的城市啊？””我本科绩点不高，能报好学校吗？““我跨考计算机，选哪个学校合适啊？”我的天……，我感觉我要在...",
        date: "2019-08-17",
        read: 22,
        interactive: 11,
        comment: "2"
      },
      {
        id: 2,
        title: "真的，Kafka 入门一篇文章就够了",
        summary:
          "初识 Kafka什么是 KafkaKafka 是由 Linkedin 公司开发的，它是一个分布式的，支持多分区、多副本，基于 Zookeeper 的分布式消息流平台，它同时也是一款开源的基于发布订阅模式的消息引擎系统。Kafka 的基本术语消息：Kafka 中的数据单元被称为消息，也被称为记录，可以把它看作数据库表中某一行的记录。批次：为了提高效率， 消息会分批次写入 Kafka，批次...",
        date: "2019-05-17",
        read: 21,
        interactive: 1,
        comment: "1"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      },
      {
        id: 3,
        title: "SpringBoot：认认真真梳理一遍自动装配原理",
        summary:
          "前言Spring翻译为中文是“春天”，的确，在某段时间内，它给Java开发人员带来过春天，但是随着我们项目规模的扩大，Spring需要配置的地方就越来越多，夸张点说，“配置两小时，Coding五分钟”。这种纷繁复杂的xml配置随着软件行业一步步地发展，必将逐步退出历史舞台。SpringBoot介绍来自：百度百科Spring Boot是由Pivotal团队提供的全新框架，其设计目...",
        date: "2019-05-17",
        read: 334,
        interactive: 153,
        comment: "18"
      }
    ];
    this.blogs = blogTest;
  }
};
</script>

<style scoped>
.home {
  width: 60%;
  margin: auto;
}
</style>
