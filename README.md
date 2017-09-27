# TClock
###  Hello,这是一个时钟圆环自定义View
  不仅有好看的样式,而且支持触控事件,每次点击、滑动然后松手的时候,判断触控区间(12区间),
  根据区间显示选中时间以及产生包含对应参数的回调事件.支持开发者的自定义需求.<br>
  另外该控件支持多达25+种属性的设置,你可以设置项目需要的样式.</br>
###  预览图
  <img width="350"  src="https://github.com/HoldMyOwn/TClock/blob/master/preview/clock-6.gif"/><br>
  大概演示,详见各个Activity</br>
  
 
 ## Attributes属性（xml中指定）
 |属性|格式|描述
 |---|---|---|
 |big_circle_color|color|大圆颜色
 |big_circle_width|integer|大圆厚度
 |big_circle_shader2|color|大院渲染色一(可以不设置)
 |big_circle_shader_show|color|大圆渲染色二(可以不设置)
 |small_circle_color|color|小圆颜色
 |small_circle_radius|dimension|小圆半径
 |small_circle_show|boolean|小圆是否显示
 |point_radius|dimension|时钟点半径
 |point_color|color|时钟点颜色
 |point_radius_choose|dimension|时钟点选中时候半径
 |point_color_choose|color|时钟点选中时候颜色
 |point_radius_ratio|float|时钟点到圆心的距离(按半径百分比)
 |arc_width|dimension|圆弧宽度
 |arc_color|color|圆弧颜色
 |arc_show|boolean|圆弧是否显示
 |center_msg_Size|dimension|中间字体大小
 |center_msg_Color|color|中间字体颜色
 |center_msg_show|boolean|中间字体是否显示
 |num_radius|dimension|时钟数字大小
 |num_color|color|时钟数字颜色
 |num_radius_choose|dimension|时钟数字选中时候大小
 |num_color_choose|color|时钟数字选中时候颜色
 |num_radius_ratio|float|时钟数字到圆心的距离(按半径百分比)
 |num_show|boolean|数字是否显示
 
 
 
 
###  事件监听
   
    //监听范围:圆环中心为中心,圆环半径的1.1倍为半径范围的圆
    //只有在up事件触发时候才进行回调,防止事件的超频率不合规触发.
    @Override
    public void onTClockTouchUp(int clockNum) {
       //参数为当前选择的时间点
       //可以做一些网络请求操作(推荐使用retrofit+rxjava通过订阅方式,
       // 处理最新的TouchUP回调,取消订阅以前的触控回调)
    }
    
###   具体细节用法,下载查看Demo</br>
###   模板依赖:&nbsp;&nbsp;项目里面的TClcok模板(可更加灵活扩展)</br>
###   gradle依赖:&nbsp;&nbsp;&nbsp;compile&nbsp;'com.jkt:tclock:1.0.1'</br>

