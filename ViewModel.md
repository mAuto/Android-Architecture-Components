# Android Architecture Components ------> ViewModel

<0> 读了Android Architecture Components ViewModel的官方文档之后，至少有下几个问题需要弄清楚
    a 如何保证ViewModel不泄露
    b ViewModel是如何做到与Actiivty和Framgent的分离的
    c Activity的重新创建(横竖屏切换)并不会造成ViewModel的丢失，是如何做到的

<1> ViewModel是一个只有一个方法(不是抽象方法)的抽象类。方法的注释是这样写的：
    /**
     * This method will be called when this ViewModel is no longer used and will be destroyed.
     * <p>
     * It is useful when ViewModel observes some data and you need to clear this subscription to
     * prevent a leak of this ViewModel.
     */
这个方法会在ViewModel不再被使用的时候调用，并且ViewModel将会被销毁。当ViewModel监听了某些数据而你需要避免泄露的时候，这个方法就会很有用。

<2> 生成一个ViewModel
    ViewModelProviders
    ViewModelProvider
    ViewModelStores
    ViewModelStore
    HolderFragment
    
