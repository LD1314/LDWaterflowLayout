# LDWaterflowLayout
瀑布流

#界面展示
![image](https://github.com/LD1314/LDWaterflowLayout/raw/master/1.png)

#使用方法
1.遵守LDWaterflowLayoutDelegate协议

2.创建LDWaterflowLayout对象,设置delegate.

3.创建UICollectionView对象,并且设置collectionViewLayout为LDWaterflowLayout.


实现LDWaterflowLayoutDelegate中的方法

@required

/** 返回每个Item的高度 */

\- (CGFloat)waterflowLayout:(LDWaterflowLayout *)waterflowLayout heightForItemAtIndex:(NSUInteger)index itemWidth:(CGFloat)itemWidth;

@optional

/** 返回的列数，默认为3 */

\- (CGFloat)columnCountInWaterflowLayout:(LDWaterflowLayout *)waterflowLayout;

/** 每一列之间的间距，默认为10 */

\- (CGFloat)columnMarginInWaterflowLayout:(LDWaterflowLayout *)waterflowLayout;

/** 每一行之间的间距，默认为10 */

\- (CGFloat)rowMarginInWaterflowLayout:(LDWaterflowLayout *)waterflowLayout;

/** 边缘的间距，默认为10 */

\- (UIEdgeInsets)edgeInsetsInWaterflowLayout:(LDWaterflowLayout *)waterflowLayout;