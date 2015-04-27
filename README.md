


    Charlin出框架的目标：简单、易用、高度封装、绝对解耦！

# CoreNewFeatureVC
版本新特性



####框架特性：<br />
>1.封装并简化了版本新特性启动视图！<br />
>2.添加了版本的本地缓存功能<br />
>3.集成简单，使用方便，没有耦合度<br />
>4.支持block回调。<br />

####重要代码：<br />
    //判断是否需要显示：（内部已经考虑版本及本地版本缓存）
    BOOL canShow = [CoreNewFeatureVC canShowNewFeature];
    
    //测试代码，正式版本应该删除
    canShow = YES;
    
    if(canShow){
        
        NewFeatureModel *m1 = [NewFeatureModel model:[UIImage imageNamed:@"f1"]];
        
        NewFeatureModel *m2 = [NewFeatureModel model:[UIImage imageNamed:@"f2"]];
        
        NewFeatureModel *m3 = [NewFeatureModel model:[UIImage imageNamed:@"f3"]];
        
        window.rootViewController = [CoreNewFeatureVC newFeatureVCWithModels:@[m1,m2,m3] enterBlock:^{
            NSLog(@"结束回调");
        }];
    }else{
        UIViewController *vc = [[UIViewController alloc] init];
        vc.view.backgroundColor = [UIColor brownColor];
        window.rootViewController = vc;
    }
  
  
  

<br /><br /><br /><br />

-----
    CoreNewFeatureVC 版本新特性。
-----

<br /><br />

#### 版权说明 RIGHTS <br />
作品说明：本框架由iOS开发攻城狮Charlin制作。<br />
作品时间： 2015.03.26 17:00<br />

#### 关于Chariln INTRODUCE <br />
作者简介：Charlin-四川成都华西都市报旗下华西都市网络有限公司技术部iOS工程师！<br /><br />


#### 联系方式 CONTACT <br />
Q    Q：1761904945（请注明缘由）<br />
Mail：1761904945@qq.com<br />
