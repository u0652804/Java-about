# Java

# 物件導向三大特性
 - 封裝(Encapsulation)
 - 繼承(Inheritance)
 - 多型(Polymorphism)
 
 ## 封裝
 目的是將 Class 裡的屬性用 private 隱藏，只能透過public的方法存取資料。
 (隱藏程式細節，避免直接處理造成的困擾。使開發與維護更容易)
 例舉: 不需要知道電腦啟動的原理，只需要按下電源鍵就可以開機．
 
 ### code
 
public class Encapsulation{
    private int value = 0;
    
    public void ChangeValue(int vale)
    {
        this.value = val;
    }
}

Encapsulation encapsulation = new Encapsulation();
//do change value
encapsulation.value = 10;//xx
encapsulation.ChangeValue(10);//oo

 
 
 
 ## 繼承
 目的是要達到「程式碼再用」(Code Rause) 或「介面再用」。
 透過繼承，可以適當的切割類別，並在衍生類別中重複使用、擴充和修改基底類別中定義的行為，又不破壞原先基底類別設計。
 
  ### code
 
public class Inheritance extends InherParent{
    int selfVal = 0;
}
 
 ## 多型
 多型 (Polymorphism) 指的是不同型態的物件，定義相同的操作介面，由於被呼叫者 (Callee) 有著相同的介面，呼叫者並不用指
 定特別型別，只需針對介面進行操作，實際執行的物件則在runtime決定，藉此增加程式碼的彈性。
 
 ## 引用
 http://stan-blog.logdown.com/posts/471289-what-is-the-inheritance
 </br>

## about static
靜態(配置記憶體)，宣告為static的變數具有唯一值，並且會固定存放於宣告時配置的記憶體位置．

![javaAbout-static](/image/javaAbout-static.png)

## about final
最後的(值)，相當於常數(在宣告final時一定得給予初始值，並且無法在後續改變數值)

![javaAbout-final](/image/javaAbout-final.png)

