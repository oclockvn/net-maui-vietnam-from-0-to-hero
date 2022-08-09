# Đôi chút lịch sử và so sánh

Hình ảnh mang tính chất minh họa:

![image](https://user-images.githubusercontent.com/3783976/183669197-28a9873a-dec4-437e-92b1-bd2a32312dff.png)

Đây cũng là bức tranh mô tả về .NET MAUI, bạn có thể build mobile app (Android/iOS) và cả desktop app (Windows/Mac) sử dụng single code base.

## Về mobile, so với Xamarin Forms (XF)

> .NET MAUI is the evolution of Xamarin.Forms  
> 
> -- [The New .NET Multi-platform App UI](https://devblogs.microsoft.com/xamarin/the-new-net-multi-platform-app-ui-maui/#:~:text=.NET%20MAUI%20is%20the%20evolution%20of%20Xamarin.Forms)

như vậy có thể thấy MAUI như là 1 bản "nâng cấp" của XF vậy. Thực tế bạn có thể migrate từ XF qua MAUI 1 cách dễ dàng mà không cần phải viết lại toàn bộ ứng dụng.
Đây là 1 lợi thế lớn cho những ai đã có kinh nghiệm về XF, có thể dễ dàng bắt đầu với MAUI mà không gặp chút khó khăn gì.

## Về Windows Desktop app, so với WPF

Ra đời cách đây hơn (có lẻ) [15 năm](https://en.wikipedia.org/wiki/Windows_Presentation_Foundation#:~:text=November%C2%A021%2C%202006%3B%2015%20years%20ago), WPF là công
nghệ được sử dụng để build desktop app có những cải tiến đáng kể so với Windows Form (WF). Cũng vì WPF và MAUI đều có thể build được desktop app, và sử dụng các kỹ thuật
tương tự nhau (XAML, data binding, ...) nên khi đưa ra lựa chọn để xây dựng ứng dụng, có thể bạn sẽ hơi bối rối. Dưới đây là 1 vài so sánh đơn giản giúp bạn có thêm nhiều góc nhìn để lựa chọn.

**WPF**
- Pros:
  - Vì lâu đời nên độ ổn định tốt
  - Có nhiều thư viện UI hỗ trợ
  - Có thể custom được nhiều loại control (ví dụ MAUI không custom được button content)
  - Có design preview cho XAML
- Cons:
  - UI hơi chuối :)

**MAUI**
- Pros:
  - Navigation built-in với animation và navigation button trên UI, navigation api friendly cho dev
  - UI được đồng nhất với fluent design style của MS
- Cons:
  - Ít control hơn
  - Không custom được content cho 1 số control là 1 bất lợi lớn (ví dụ button)
  - Không có design preview cho XAML (bù lại có hot reload nhưng WPF trên .NET Core cũng đã support)
  - Còn khá nhiều lỗi về UI

Một số điểm khác có thể kể tới mặc dù không quá khác biệt:
- MAUI được built-in dependency injection, WPF cần thêm 1 số step
- WPF có nhiều tutorial và document hơn, nhưng cơ bản MAUI cũng có thể xem những document đó vì đa số là về XAML

Với những khác biệt trên, để đưa ra lựa chọn cũng không mấy khó khăn:
- WPF: chỉ khi mình chắc chắn 100% là application của mình chỉ được xài trên Windows và không mấy quan tâm về UI :))
- MAUI: các trường hợp còn lại. Công nghệ mới, UI xịn, tội gì mà không triển.

## Đôi chút so sánh với flutter
[Flutter](https://flutter.dev/multi-platform) là công nghệ của Google dùng để build multiple platforms application (Android/iOS/Windows/Mac và kể cả Embedded Devices).
Những điểm mạnh của Flutter có thể kể tới như:
- Được viết bằng Dart, là ngôn ngữ dễ học, đơn giản
- Declarative UI, UI by code nên support intellisense tốt
- Hot reload, live reload làm tăng development experience
- Và nhiều thứ khác nữa

So với .NET MAUI có thể thấy:
- UI được design bằng XAML và handle logic bằng code behind làm tăng lộ trình học cho dev (UI vẫn có thể được develop bằng C# thông qua markup extension nhưng vẫn prefer XAML)
- MVVM là mô hình được áp dụng nhiều nhất cho MAUI, cũng tăng lộ trình học cho dev
- Data binding không support tốt trong 1 số trường hợp làm tăng khả năng đánh đồng nghiệp cho dev

Với những sự khác biệt trên, dễ thấy Flutter được recommend hơn nếu lựa chọn công nghệ để build multiple platforms app. Tuy nhiên MVVM, XAML và .NET vẫn là cái
gì đó lôi cuốn những người điên khiến họ cứ dấn thân vào MAUI.

Nếu bạn cũng điên thì xin chờ bài tiếp theo vào 1 ngày không xa.
