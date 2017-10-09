# 项目中的TAG标签库使用

## 1.region地区标签使用
  
![cmd-markdown-logo](http://chuantu.biz/t6/86/1507529363x2061759526.png)

  引入：<%@ taglib uri="http://www.gttown.com/options" prefix="opt" %>，如图：
  
  ![cmd-markdown-logo](http://chuantu.biz/t6/86/1507529562x2061759526.png)
  
  写法：<opt:region code="330000"/>，code代表地区代码。

## 2.country国家标签使用
tld文件引入：
    <tag>
        <name>country</name>
        <tag-class>com.gttown.common.support.tag.GttownCountryTag</tag-class>
        <body-content>JSP</body-content>
        <attribute>
            <name>name</name>
            <required>true</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
        <attribute>
            <name>chinese</name>
            <required>false</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
    </tag>
jsp引入标签：<%@ taglib uri="http://www.gttown.com/gttown-app/tags" prefix="gttown" %>
    
写法：<gttown:country name="${country}" chinese="false"/>

name为需要存入的国家代码，chinese参数true为中文,false为英文。

## 3.获取常量配置信息 common.properties
tld文件引入：
    <function>
        <name>env</name>
        <function-class>com.gttown.common.util.Env</function-class>
        <function-signature>java.lang.String getValue(java.lang.String)</function-signature>
        <description>获取常量配置信息 common.properties</description>
    </function>
写法：${gttown:env('staticDomain')}。staticDomain为需要获取的配置key

## 4.列表分页标签
tld文件引入：
    <tag>
        <name>Page</name>
        <tag-class>com.gttown.common.tag.PaginationTag</tag-class>
        <body-content>empty</body-content>
        <attribute>
            <name>pager</name>
            <required>true</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
        <attribute>
            <name>centerPage</name>
            <required>false</required>
            <rtexprvalue>false</rtexprvalue>
        </attribute>
        <attribute>
            <name>formId</name>
            <required>false</required>
            <rtexprvalue>false</rtexprvalue>
        </attribute>
        <attribute>
            <name>ajax</name>
            <required>false</required>
            <rtexprvalue>false</rtexprvalue>
        </attribute>
    </tag>
写法：<gttown:Page pager="${pager}" centerPage="10"/>。pager为分页对象名称。

## 5.企业行业类型标签
  tld文件引入：
     <tag>
        <name>industryType</name>
        <tag-class>com.gttown.common.support.tag.IndustryType</tag-class>
        <body-content>JSP</body-content>
        <attribute>
            <name>value</name>
            <required>true</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
        <attribute>
            <name>lang</name>
            <required>false</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
    </tag>
  写法：<gttown:industryType value="${com.industryType}" lang="en"/>。lang参数可以为en或者zh-CN。
## 6.企业性质标签
  tld文件引入：
    <tag>
        <name>EnterpriseType</name>
        <tag-class>com.gttown.common.support.tag.EnterpriseType</tag-class>
        <body-content>JSP</body-content>
        <attribute>
            <name>type</name>
            <required>true</required>
            <rtexprvalue>true</rtexprvalue>
        </attribute>
    </tag>
  写法：<gttown:industryType value="${enterprise.industryType}"/>。value为企业性质代码。

## 7.获取常用User
 tld文件引入：
    <tag>
        <name>loginUser</name>
        <tag-class>com.gttown.common.tag.GttownUser</tag-class>
        <body-content>empty</body-content>
    </tag>
 写法：<gttown:loginUser/>
    
