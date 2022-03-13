# JYScrollCollectionview
pageControl是滑动一整页，该app每次滑动一个cell的宽度
![image](https://img-blog.csdnimg.cn/2021011012545317.gif)




也可以添加collectionView.contentInset = UIEdgeInsetsMake(0, 30, 0, 0);
设置左边小右边大的效果

代码是用纯OC写成

如果这个代码帮到你的话，欢迎Star，谢谢


============== ysy分割线 ==============

这个是实现了分页的效果，但是滚动效果上不是很流畅，能够感觉到明显的卡顿

还有就是 - (void)scrollViewHandleScrollWithScrollView:(UIScrollView *)scrollView 这个方法是因为 scrollViewDidEndDragging 和 scrollViewWillBeginDecelerating 执行两次

还有就是计算上要很小心，如果collectionView开始设置了contentInset，contentOffset.x 取值上就要注意

更好的方法，还是去重写 UICollectionViewFlowLayout，体验上会更好，也更通用。

参考地址：https://github.com/yanshiyu/HorizontalPageView
