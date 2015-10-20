# Github Flavored Markdown 语法

## 目的

   **总结对标准的Markdown语法增强部分**

## GFM
    
1. 单词中的含有下划线时，GFM 会忽略,不转换成斜体
    
   示例:   
   ` wow_great_stuff`  
   若将字符串中的某个单词变成斜体,则可以使用\*  
   ` wow*great*stuff`
      
   效果:  
    wow_great_stuff  
    wow*great*stuff
        
2. 自动识别URL连接  
    示例:  
    `http://example.com`  
    效果:  
    http://example.com  
    
3. 删除线  
    示例:  
    `~~Mistaken text.~~`  
    效果:  
   ~~Mistaken text.~~ 

4. 代码段每行使用4个空格,标准MD会自动识别为代码段,GFM也支持这样的语法
   同时GFM还设计了一种优化语法,就是在代码段头尾行使用 `  
   还支持语言标识

   示例: 
  
        	 ```javascript
        	 function test() {
        	 console.log("notice the blank line before this function?");
        	 }
        	 ```
  
   效果:
  
    ```javascript
      function test() {
        console.log("notice the blank line before this function?");
      }
    ```
5. 支持表格
  * 基本:  
    示例：
    ```
    First Header | Second Header  
    -------------|--------------   
    Content Cell | Content Cell  
    Content Cell | Content Cell  
    ```
    
    效果:
    
    First Header | Second Header
    -------------|--------------
    Content Cell | Content Cell
    Content Cell | Content Cell
    

  * 可以在两边都加竖线:

    示例:
    
    ```
    | First Header  | Second Header |  
    | ------------- | ------------- |  
    | Content Cell  | Content Cell  |  
    | Content Cell  | Content Cell  |  
    ```
    
    效果:
  
    | First Header  | Second Header |
    | ------------- | ------------- |
    | Content Cell  | Content Cell  |
    | Content Cell  | Content Cell  |

  * 可以不对齐:

    示例:  

    ```
    | Name | Description          | 
    | ------------- | ----------- |  
    | Help      | ~~Display the~~ help window.|   
    | Close     | _Closes_ a window     |   
    ```

    效果:

    | Name | Description          |
    | ------------- | ----------- |
    | Help      | ~~Display the~~ help window.|
    | Close     | _Closes_ a window     |

  * 可以定义表格中文字对齐方式:

    示例:  
    ```
    | Left-Aligned  | Center Aligned  | Right Aligned |  
    | :------------ |:---------------:| -----:|  
    | col 3 is      | some wordy text | $1600 |  
    | col 2 is      | centered        |   $12 |  
    | zebra stripes | are neat        |    $1 |  
    ```

    效果:  
    
    | Left-Aligned  | Center Aligned  | Right Aligned |
    | :------------ |:---------------:| -----:|
    | col 3 is      | some wordy text | $1600 |
    | col 2 is      | centered        |   $12 |
    | zebra stripes | are neat        |    $1 |

  * 支持在表格中嵌入图片
    示例:  
    ```
    | 图片|描述|
    | ------------ |---------------|
    | http://img4.duitang.com/uploads/item/201508/19/20150819131018_vYPyR.thumb.224_0.png  | Overload 森林贤王——仓助        |
    ```

    效果:  
    
    | 图片|描述|
    | ------------ |---------------|
    |![仓助](http://img4.duitang.com/uploads/item/201508/19/20150819131018_vYPyR.thumb.224_0.png) | Overload 森林贤王——仓助        |

6. Task列表

   *GFM 支持把列表变成带勾选的任务列表* 
   
   * 基本列表

    示例:

    ```
    - [ ] a task list item
    - [ ] list syntax required
    - [ ] normal **formatting**, @mentions, #1234 refs
    - [ ] incomplete
    - [x] commplete
    ```

    效果:

    - [ ] a task list item
    - [ ] list syntax required
    - [ ] normal **formatting**, @mentions, #1234 refs
    - [ ] incomplete
    - [x] commplete

    * 嵌套列表

    示例2:

    ```
    - [ ] a bigger project
      - [ ] first subtask #1234
      - [ ] follow up subtask #4321
      - [ ] final subtask cc @mention
    - [ ] a separate task
    ```

    效果:
    - [ ] a bigger project
      - [ ] first subtask #1234
      - [ ] follow up subtask #4321
      - [ ] final subtask cc @mention
    - [ ] a separate task


7. 添加表情
    
     *GFM支持天假emoji表情,输入不同的符号码表示不同的表情*

    示例:

    ```
    :blush:
    :joy:
    :grinning:
    ```

    效果:

    :blush:
    :joy:
    :grinning:
