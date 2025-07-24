# Data-Structure  41143224
# 問題一(阿克曼函數)
# 解題說明
此為阿克曼函數直接依照題目的要求寫出遞迴，假設m=3,n=4即為條件三開始執行一層一層最終m=0 n擔任了執行次數的角色。若不使用遞迴則能使用堆疊只要條件符合就把數值丟進去n並在條件一一成立時值行相對應的動作，並設計n堆疊頂端為
-1並且m堆疊沒有資料便輸出一直在累加的n。
# 程式實作
```
#include iostream
using namespace std;
int Ackerman(int m, int n) {
    if (m == 0) {
        return n + 1;
    } else if (m > 0 && n == 0) {
        return Ackerman(m - 1, 1);
    } else if (m > 0 && n > 0) {
        return Ackerman(m - 1, Ackerman(m, n - 1));
    }
}

int main() {
    int result;
    result = Ackerman(2, 3);
    cout << "Ackerman(2, 3) = " << result << endl;
    return 0;
}\\遞迴
```
# 效能分析
<img width="526" height="61" alt="螢幕擷取畫面 2025-07-24 152916" src="https://github.com/user-attachments/assets/6d159855-79b4-424f-92b2-1fc351570865" />
