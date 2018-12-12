# Java

# 物件導向三大特性
 - 封裝(Encapsulation)
 - 繼承(Inheritance)
 - 多型(Polymorphism)
 
## 封裝
目的是將 Class 裡的屬性用 private 隱藏，只能透過public的方法存取資料。
(隱藏程式細節，避免直接處理造成的困擾。使開發與維護更容易)
 
例舉: 不需要知道電腦啟動的原理，只需要按下電源鍵就可以開機．

### Java code
### class Encapsulation
    public class Encapsulation{
        private int value = 0;
        
        public void ChangeValue(int vale)
        {
            this.value = val;
        }
    }
### main
    Encapsulation encapsulation = new Encapsulation();
    //do change value
    encapsulation.value = 10;//xx
    encapsulation.ChangeValue(10);//oo

 
## 繼承
目的是要達到「程式碼再用」(Code Rause) 或「介面再用」。
透過繼承，可以適當的切割類別，並在衍生類別中重複使用、擴充和修改基底類別中定義的行為，又不破壞原先基底類別設計。
 
### Java code
### parent class
    public class InherParent {
        public int val = 0;//父類別的參數
    }
### child class
    public class Inheritance extends InherParent{
        int selfVal = 0;//子類別(自己)的參數
    }
### main
		//Inheritance
		System.out.println("Inheritance : ");
		System.out.println("----------------------");
		
		Inheritance inher1 = new Inheritance();
		inher1.val = 10;
		System.out.println("inher val : " + inher1.val);// 使用子類別(自己)的參數或方法
		System.out.println("inher selfval : " + inher1.selfVal);// 可使用繼承(extends)來自父類別的參數或方法
 
 
## 多型
多型(Polymorphism)，簡單來說就是同名的方法。多個相同名稱的方法，傳入不同的參數，會執行不同的敘述。 比方說，一個計算面積的方法，如果傳入一個參數，就當正方形來算面積；傳入兩個參數，就當成長方形來算面積。

### Java code
### class
    public class Polymorphism {
    	
    	public void polyTest(int a)
    	{
    		System.out.println("input have 1 data : a = " + a);
    	}
    	
    	public void polyTest(int a, int b)
    	{
    		System.out.println("input have 2 data : a = " + a + " b = " + b);
    	}
    
    }
### main
		System.out.println("Polymorphism's Overloading : ");
		System.out.println("----------------------");
		
		Polymorphism poly1 = new Polymorphism();
		poly1.polyTest(2333);
		poly1.polyTest(2333, 66666);
		System.out.println("\n");

 
 ## 引用
 http://stan-blog.logdown.com/posts/471289-what-is-the-inheritance
 
 https://noob.tw/java-oop/
 </br>

## about static
靜態(配置記憶體)，宣告為static的變數具有唯一值，並且會固定存放於宣告時配置的記憶體位置．

![javaAbout-static](/image/javaAbout-static.png)

## about final
最後的(值)，相當於常數(在宣告final時一定得給予初始值，並且無法在後續改變數值)

![javaAbout-final](/image/javaAbout-final.png)

## Difference between ArrayList and vector in java
ArrayList和vector都以陣列做為數據結構。

差異性:
 - ArrayList是非同步的(多執行緒可以同時訪問它); vector是同步的(在多執行緒下會進行綁定，同一時間只能有一個執行緒訪問它)。
 多執行緒下為了線程安全，較適合使用vector。
 
 - Resize: ArrayList和vector都可以動態增加大小。差別在於ArrayList增長現有大小的一半; vector則是增長為現有大小的兩倍。
 
 - 效能: ArrayList效能較好; vector為了線程安全的問題，所以效能較差。
 
