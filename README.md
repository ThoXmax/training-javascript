# Javascript

### 寬鬆模式 vs 嚴格模式

* 一般模式(non-strict mode): 
    
    給予開發者相當大的寬容，針對可能有問題或妨礙最佳化的語意，不會特別跳出警告。
    
* 嚴格模式(strict mode):
    
    會啟動更嚴格的標準，會在console裡丟出更多的警告，甚至禁止使用某些未來會消失的語法。
    
    嚴格模式可以在:
    * 整份文件的最上方宣告
    * 函式(function)的開頭宣告 

### Coding Style

* Javascript Standard Style Guide
    * 2格縮排
    * 字串使用單引號
    * 沒有未使用的變數(每一個宣告的變數，都要被使用)
    * 沒有分號
    * 關鍵字後加空白
    * 函式名稱後加空白
    * 永遠使用 ===

* 程式碼自動修訂
    * JSLint
    * ESlint(ES6)

### 變數與作用範圍

* 基本型別(單一值): 數字、字串、布林值、undefined、null。
* 物件型別: 陣列、函式。
* 作用範圍: 子層可存取父層，父層讀取不到子層變數。水平區塊(block)的變數不可互相存取。

* 檢查型別: 
    
    Q:若要將兩變數做運算，但卻不清楚變數的型別
    ```javascript
        if (typeof a === typeof b) {
            console.log(a + b)
        } else {
            console.log('x')
        }
    ```
    
    False: 0、NaN、''、false、null、undefined。
    
* 陣列操作方法:
    ```javascript
        // 宣告陣列
        const nums = [1, 2, 3]
        
        // 陣列前插入數字(unshift)
        nums.unshift(0)
        console.log(nums) → [0, 1, 2, 3]
        
        // 陣列前取出數字(shift)
        nums.shift()
        console.log(nums) → [1, 2, 3]
        
        // 陣列後取出數字(pop)
        nums.pop()
        console.log(nums) → [1, 2]
        
        // 陣列後插入數字(push)
        nums.push(2, 4)
        console.log(nums) → [1, 2, 2, 4]
        
        // 陣列中插入數字(splice(插入位置, 刪除的數字, 插入的值))
        nums.splice(1, 1, 87)
        console.log(nums) → [1, 87, 2, 4]
        
        nums.splice(2, 1) // 刪除第3個參數
        console.log(nums) → [1, 87, 4]
        
        nums.slice(0, 3) // 回傳前3個值的陣列
        
        nums.slice(3) // 剔除前3個值得陣列
        
        // 合併元素(concat)
        nums.concat([1, 2, 4])
        console.log(nums) → [1, 87, 4, 1, 2, 4]
        
        *** 若使用concat並不會修改到原本的陣列, 但若使用push則會修改到原本的陣列 ***
        
    ```
   
 * 物件操作方法:
    ```javascript
        
        // 宣告物件
        const user = {
            name: 'Max',
            age: 30,
            features: ['handsome', 'tall'],
            skill: {
                frontEndSide: ['html', 'css', 'javascript'],
                backEndSide: ['x']
            }
        }
        
        // 查詢資料
        user.name → 'Max'
        user['name'] → 'Max'
        
        // 寫入新的屬性
        user.car = 'BMW'
        user['car'] = 'BMW'
        
        // 列出所有的值: for-in 迴圈
        for (let key in user) {
            console.log(user[key])
        }
        
        // 取出所有的key值 - Object.keys()
        // 取出所有的value - Object.values()
        // 取出所有的pair - Object.entries()
    ```
   




