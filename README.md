> #### 作者主页：[舒克日记](https://blog.csdn.net/cativen)
>
>  简介：Java领域优质创作者、Java项目、学习资料、技术互助
>
> <b><font color=red>文中获取源码</font></b>

# 项目介绍



后台：
1.登录：输入账号、密码，即可登录。
2.套房管理：可对房间房型进行管理。
3.入住管理：可对客户入住状态进行管理。
4.订单管理：对用户已提交的订单进行管理。
5.员工管理：对酒店员工进行管理。
6.评论管理：对用户评论进行管理。





前台：
1.登录：输入账号、密码，即可登录。
2.套房预订：用户可以通过浏览套房进行了解并在线预订。 
3.酒店详情：用户可以查询酒店的政策与设施，以及网友评价。
4.订单中心：用户可以查询自己的订单信息。
5.个人信息：编辑修改个人信息



# 环境要求

1.运行环境：最好是java jdk1.8,我们在这个平台上运行的。其他版本理论上也可以。 

2.IDE环境：IDEA,Eclipse,Myeclipse都可以。推荐IDEA; 

3.tomcat环境：Tomcat7.x,8.X,9.x版本均可 

4.硬件环境：windows7/8/10 4G内存以上；或者Mac OS; 

5.是否Maven项目：是；查看源码目录中是否包含pom.xml;若包含，则为maven项目，否则为非maven.项目 

6.数据库：MySql5.7/8.0等版本均可；



# 技术栈

运行环境：jdk8 + tomcat9 + mysql5.7 + windows10

服务端技术：Spring Boot+ Mybatis +VUE



# 使用说明

1.使用Navicat或者其它工具，在mysql中创建对应sq文件名称的数据库，并导入项目的sql文件； 

2.使用IDEA/Eclipse/MyEclipse导入项目，修改配置，运行项目； 

3.将项目中config-propertiesi配置文件中的数据库配置改为自己的配置，然后运行；

# 运行指导

idea导入源码空间站顶目教程说明(Vindows版)-ssm篇：

http://mtw.so/5MHvZq 

源码地址：[http://www.codegym.top](http://www.codegym.top/)



# 运行截图

## 文档截图

![img](https://img-blog.csdnimg.cn/img_convert/e0c12f85c0df6432ae5cc9951d399eb0.png)



![springboot221酒店管理系统1](https://img-blog.csdnimg.cn/img_convert/7470504a2c33ef8ca718851f2d38cc70.png)

![springboot221酒店管理系统2](https://img-blog.csdnimg.cn/img_convert/84167d3bc36502a8886fd06ba7b9c593.png)

![springboot221酒店管理系统3](https://img-blog.csdnimg.cn/img_convert/9b3d2c44c014b73ca7d502bc2e611c55.png)

![springboot221酒店管理系统4](https://img-blog.csdnimg.cn/img_convert/8e16b16620cdab94381026c87d7830cb.png)



![springboot221酒店管理系统5](https://img-blog.csdnimg.cn/img_convert/c225225d4221d66db78fedee045627a3.png)


### 代码

```java
public class Solution {
    public List<Integer> count(List<Set<Integer>> lists) {
        Map<Integer, Integer> countMap = new HashMap<>();

        // 遍历每个 Set<Integer> 并更新每个数字的出现次数
        for (Set<Integer> set : lists) {
            for (Integer num : set) {
                countMap.put(num, countMap.getOrDefault(num, 0) + 1);
            }
        }

        // 找出出现次数大于10次的数字
        List<Integer> result = new ArrayList<>();
        for (Map.Entry<Integer, Integer> entry : countMap.entrySet()) {
            if (entry.getValue() > 10) {
                result.add(entry.getKey());
            }
        }

        return result;
    }

    public static void main(String[] args) {
        // 示例测试
        List<Set<Integer>> lists = new ArrayList<>();
        for (int i = 0; i < 100; i++) {
            Set<Integer> set = new HashSet<>(Arrays.asList(i, i + 1, i + 2, 50));
            lists.add(set);
        }

        Solution solution = new Solution();
        List<Integer> result = solution.count(lists);
        System.out.println(result);
    }
}

```












