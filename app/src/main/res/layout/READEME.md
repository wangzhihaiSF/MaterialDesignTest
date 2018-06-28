### RecyclerView 会将toolbar 遮挡住
由于 RecyclerView 和 Toolbar 都是放在 CoordinatorLayout 中的，而 Coordinatorlayout 是加强版的 FrameLayout，那么 FrameLayout 中所有空间在不
明确定位的情况下，默认都会摆放在布局的左上角。从而缠上遮挡现象。若是FrameLayout，唯一的解决方法就是向下偏移一个 ToolBar 的高度，而使用
 CoordinatorLayout 的话，可以使用Design Support 库中提供的 AppBarLayout。

### AppBarLayout  简介
APPBarLayout 实际上是一个垂直方向上的 LinearLayout，他在内部做了很多滚动事件的封装，应用了一些 Design Support 的设计理念。

### 解决覆盖问题
1. 将 Toolbar 嵌套到 APPBarLayout 中
2. 给 RecyclerView 指定一个布局行为
