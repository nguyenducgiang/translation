---
Author: Jeff Atwood
Translator: Nguyễn Đức Giang
---

# Mẫu đăng nhập của Chúa

> Đây là bản dịch bài viết [The God Login](http://blog.codinghorror.com/the-god-login/) của [Jeff Atwood](http://blog.codinghorror.com/) thực hiện bởi [Nguyễn Đức Giang](https://github.com/nguyenducgiang).

Tôi tốt ngiệp với bằng "minor" Khoa học Máy tính (KHMT) từ đại học Virginia (UVa) vào năm 1992. Lí do nó là bằng "minor", không phải "major" là vì để đạt được bằng "major" KHMT ở UVa, bạn phải trải qua một khóa học kĩ thuật (Engineering School), và nói một cách dễ nghe thì tôi hoàn toàn không phù hợp với các vấn đề toán học và vật lý phức tạp ở đó. Điều tuyệt vời ở khóa "minor" là tôi có thể tự do lựa chọn tất cả những lớp CS thú vị và bỏ qua tất cả những môn khác.

Một trong những lớp học ưa thích của tôi là Thuật toán, lớp học tôi nhớ nhất. Tôi luôn nói với mọi người rằng lớp học về Thuật toán là phần trong quá trình học đại học có ảnh hưởng nhiều nhất tới tôi trong sự nghiệp lập trình viên. Chính tôi cũng không rõ tại sao, nhưng vài năm trước, tôi chợt có chút cảm giác nên tìm xem [một CV](http://www.cs.cmu.edu/~pausch/Randy/Randy/Vita.html) và nhận ra Randy Pausch - vâng, [the Last Lecture Randy Pausch](http://en.wikipedia.org/wiki/The_Last_Lecture) - là giảng viên của lớp đó. Nhằm vào một thời điểm hoàn hảo: Đại học Virginia, mùa thu năm 1991, CS461 Phân tích thuật toán, 50 sinh viên.

Tôi là một trong số (50 sinh viên) đó.

Xem video [Randy Pausch Last Lecture: Achieving Your Childhood Dreams](https://youtu.be/ji5_MqicxSo)

Và chẳng còn gì khúc mắc về lí do tôi đã bị ấn tượng như vậy. Pausch là một giảng viên đáng kinh ngạc, đầy sức lôi cuốn, một minh chứng cho câu ngạn ngữ cổ rằng bạn nên chọn người thầy của mình trước khi tìm kiếm tài liệu, nếu như bạn thực sự quan tâm đến việc học. Hoàn toàn đúng đắn.

Trong trường hợp này, sự kết hợp giữa giảng viên tuyệt với chủ đề tuyệt vời làm tăng thêm sức hấp dẫn khi thuật toán là trọng tâm trong công việc của lập trình viên. Không phải ở chỗ phát minh ra các thuật toán, mà chúng tôi cần phải thấu hiểu những đoạn mã ngoài kia một cách cặn kẽ và trực quan: tại sao chúng (những đoạn mã) có xu hướng chạy nhanh hay chậm do những lựa chọn mang tính đánh đổi (nguyên bản: tradeoffs), và lựa chọn thuật toán chính xác cho những gì chúng tôi đang làm. Đây là điều tối cần thiết.

Và một trong những điều thú vị nhất Mr. Pausch từng dạy tôi là khi đặt ra câu hỏi:

> Thuật toán của Chúa cho vấn đề này là gì?

Vâng, khi sắp xếp một danh sách, rõ ràng là Chúa sẽ không bận tâm với các thuật toán ngu ngốc Bubble Sort hay Quick Sort hay Shell Sort như đám người trần mắt thịt chúng ta. Chúa chỉ việc đặt chúng vào đúng vị trí của mình ngay tức thì. Bam. Chỉ 1 bước duy nhất. [Giới hạn cực tiểu trong tính toán](http://bigocheatsheet.com/), O(1). Và hoàn toàn không tốn chút thời gian nào (cho các tính toán), bởi vì *đó là Chúa*.

![](http://blog.codinghorror.com/content/images/2015/01/god-you-asked-for-a-sign.jpg)

Tâm trí của tôi đã hoàn toàn bị chấn động ở thời điểm đó.

Tôi luôn ngờ rằng các lập trình viên đã trở thành lập trình viên vì [họ có cơ hội đóng vai Chúa trời](http://blog.codinghorror.com/bridges-software-engineering-and-god/) trong tiểu vũ trụ trên bàn làm việc của mình. Randy Pausch đã biến sự tự phụ đó thành một cách hữu ích để thiết lập các ranh giới và tự vấn mình bằng những câu hỏi khó về những gì bản thân đang làm và tại sao lại làm những việc đó.

Vì vậy, khi chúng tôi bắt đầu xây dựng một hộp thoại đăng nhập cho [Discourse](http://www.discourse.org/), tôi quay trở lại với những gì đã học trong lớp Thuật toán và tự hỏi:

> Chúa sẽ xây dựng hộp thoại đăng nhập này thế nào?

Và câu trả lời dĩ nhiên là **Chúa sẽ chẳng bận tâm đến việc làm một hộp thoại đăng nhập**. Tất cả người dùng đều sẽ được tự động đăng nhập GodApp ngay khi họ mở ứng dụng bởi vì Chúa biết rõ từng người dùng. Một cách đầy uy quyền, chính xác là vậy.

Còn với chúng tôi, việc này là bất khả thi vì Chúa không phải một trong những nhà đầu tư cho dự án.

Nhưng.. chúng tôi có thể tiến gần đến những trải nghiệm đăng nhập hoàn hảo như của Chúa *đến mức nào*? Đây là một mục tiêu thực tế và đẹp đẽ.

![](http://blog.codinghorror.com/content/images/2015/01/discourse-login-dialog.png)

Chẳng phải Bill Gates có lần [từng thắc mắc](https://www.commandprompt.com/community/pyqt/x3581) tại sao tất cả các lập trình viên lại viết đi viết lại một hộp thoại mở tệp tin giống hệt nhau? Với hộp thoại đăng nhập cũng thế. Từ cách đây khá lâu, tôi cho rằng [cách đăng nhập tốt nhất là hoàn toàn không (cần) đăng nhập](http://blog.codinghorror.com/cutting-the-gordian-knot-of-web-identity/) và tôi là một người ủng hộ trung thành của ý tưởng [đăng nhập với giấy phép Internet](http://blog.codinghorror.com/your-internet-drivers-license/) bất cứ khi nào khả dụng. Vì vậy, Discourse hoàn toàn hỗ trợ việc này, nếu như bạn thiết lập cấu hình phù hợp.

![](http://blog.codinghorror.com/content/images/2015/01/common-oauth-logins.png)

Nhưng ngày hôm nay tôi chỉ muốn tập trung vào **cốt lõi, cơ sở của trải nghiệm đăng nhập: người dùng và mật khẩu.** Đây là hình thức mặc định cho đến khi bạn cấu hình thêm các phương thức đăng nhập khác.

Một biểu mẫu đăng nhập với 2 trường, 2 nút và một liên kết, có vẻ đơn giản phải không? Theo suy nghĩ thông thường là vậy. Và nó là như vậy, cho đến khi bạn cân nhắc tất cả các trường hợp mà một hành động đăng nhập đơn giản có thể dẫn đến những bất cập cho người dùng. Chúng ta hãy cùng xem xét.

## Hãy để người dùng nhập email khi đăng nhập

Lỗi lầm chết người của OpenID, một trong những giải pháp đăng nhập xuất hiện sớm nhất mà tôi [đã từng thích](http://blog.codinghorror.com/openid-does-the-world-really-need-yet-another-username-and-password/), là cho rằng người dùng có thể chấp nhận việc dùng 1 URL làm "danh tính". Điều này hoàn toàn điên rồ, và về lâu dài nhược điểm này đã ngăn cản OpendID trở thành một tiêu chuẩn của tương lai.

**Danh tính người dùng luôn là email, rất minh bạch và giản dị**. Điều gì xảy ra khi bạn quên mật khẩu? Bạn sử dụng email, đúng không? Vì thế, email là  danh tính của bạn. Một số người thậm chí đề nghị sử dụng email làm phương thức đăng nhập duy nhất.

![](http://blog.codinghorror.com/content/images/2015/01/discourse-log-in-email.png)

Đương nhiên là tốt khi có username, nhưng hãy *luôn luôn* để người dùng đăng nhập bằng địa chỉ email hoặc username. Bởi vì tôi có thể chắc chắn 100% với bạn rằng khi người dùng quên mật khẩu, họ sẽ luôn luôn cần tới địa chỉ email để thiết lập lại mật khẩu. Email và mật khẩu là hai khái niệm có quan hệ chặt chẽ, và chúng thuộc về nhau. Luôn luôn là thế!

(Tiện đây tôi cũng bày tỏ sự không hài lòng của mình với các dịch vụ không cho phép tôi sử dụng email như là username để đăng nhập. Đặc biệt với Comixology: tôi vẫn đang chờ đấy!)

(chú thích: Comixology là một trang web lớn về comic - ND)

## Báo cho người dùng biết khi email của họ không tồn tại

OK, như vậy chúng ta biết rằng email là danh tính không chính thức của đại đa số mọi người, một điều hợp lý và cần thiết cho vấn đề đang bàn tới ở đây: hộp thoại đăng nhập. Nhưng trong số 10 email đang sở hữu, tôi đã dùng *email nào* để đăng nhập vào trang web của bạn?

Đây là ngọn nguồn của một [thảo luận sôi nổi trên Discourse](https://meta.discourse.org/t/different-password-reset-for-wrong-username-email/15909) về việc có nên để cho người dùng biết cơ sở dữ liệu của chúng tôi có hay không email mà người dùng nhập vào biểu mẫu "quên mật khẩu". Trên rất nhiều trang web, bạn sẽ thường gặp kiểu thông báo dưới đây sau khi điền email vào biểu mẫu "quên mật khẩu":

> Nếu có tài khoản khớp với name@example.com, bạn sẽ nhanh chóng nhận được email hướng dẫn thiết lập lại mật khẩu.

Chú ý từ "nếu" mập mờ ở trên, được dùng làm [rào cản ngăn chặn các vấn đề về bảo mật làm lộ thông tin về một địa chỉ email có tồn tại trên cơ sở dữ liệu của trang web hay không](Note the coy "if" there, which is a hedge against all the security implications of revealing whether a given email address exists on the site just by typing it into the forgot password form.) bằng cách điền email đó vào mẫu quên mật khẩu.

Chúng tôi cực kì nghiêm túc về việc lựa chọn chế độ mặc định an toàn cho Discourse, nên mặc nhiên bạn sẽ không bị làm phiền và lợi dụng bởi các spammer. Nhưng sau những trải nghiệm thực tế  "chúng ta đã dùng email nào ở đây nhỉ?" lặp đi lặp lại trên hàng tá các bản cài đặt Discourse của mình, chúng tôi nhận ra rằng trong trường hợp này, việc thân thiện với người dùng quan trọng hơn những lo lắng về bảo mật.

![](http://blog.codinghorror.com/content/images/2015/01/forgot-password.png)

Chế độ mặc định mới cho phép người dùng biết khi địa chỉ emal họ nhập vào biểu mẫu quên mật khẩu không tồn tại trong cơ sở dữ liệu của trang web. Điều này sẽ giúp giảm phiền toái cho cả người dùng và các bạn (người sở hữu website). Nếu vẫn còn băn khoăn về việc này, bạn có thể tăng cường bảo mật trong trong phần thiết lập của Discourse.

## Cho người dùng di chuyển giữa Đăng nhập và Đăng kí bất cứ lúc nào

Nhiều website bắt đầu hiển thị nút đăng nhập và đăng kí cạnh nhau. Điều này khiến tôi rất bối rối; chẳng phải đăng nhập và đăng kí là hai hành động rất khác nhau?

À, nhìn từ phía người dùng thì không phải vậy. Hộp thoại đăng nhập của The Verge cho thấy sự gần gũi giữa mẫu đăng kí và đăng nhập. Hãy cùng xem ảnh động bên dưới để rõ ràng hơn.  

![](http://blog.codinghorror.com/content/images/2015/01/login-vs-sign-up.gif)

Chúng tôi nhìn nhận sự tương đồng này với việc cho phép truy cập một trong hai biểu mẫu bất cứ lúc nào thông qua hai nút ở phía dưới biểu mẫu, sử dụng kĩ thuật tắt mở (toggle):

![](http://blog.codinghorror.com/content/images/2015/01/login-vs-create-new-account.png)

Và cả hai có thể được truy cập từ bất kì trang nào thông qua hai nút "Sign Up" và "Log In" ở góc phải trên đầu trang.

![](http://blog.codinghorror.com/content/images/2015/01/sign-up-vs-log-in-discourse.png)

## Lựa chọn các từ thông dụng

Vấn đề với ngôn ngữ (tiếng Anh) là chúng ta có quá nhiều *từ* cho các khái niệm:

- Sign In
- Log In
- Sign Up
- Register
- Join <site>
- Create Account
- Get Started
- Subscribe

Đâu là từ "chuẩn"? [Dữ liệu nghiên cứu người dùng cũng không chắc chắn về điều này](http://ux.stackexchange.com/questions/1080/using-sign-in-vs-using-log-in).

Tôi thiên về các phiên bản ngắn hơn khi có thể, chủ yếu vì tôi thích các thứ ngắn gọn, nhưng có những trường hợp cho mỗi từ trên phù hợp với hoàn cảnh và sở thích của người dùng.

![](http://blog.codinghorror.com/content/images/2015/01/bad-okay-good-login-buttons.png)

"Sign in" có thể phổ thông hơn một chút, dù "Log In" có [nguồn gốc  từ lịch sử hàng hải và máy tính](http://www.designcult.org/2011/08/why-do-we-call-in-logging-in.html) làm cho nó vẫn có giá trị nhất định:

>Cách đây vài năm tôi làm một khảo sát trên các trang web hàng đầu ở US và UK để tìm hiểu xem họ sử dụng "sign in", "log in", "login", "log on" hay các biến thể khác. Kết quả tại thời điểm đó là nếu như bạn tính "log in" và "login" làm một thì số lượng vượt quả "sign in", nhưng không nhiều. Tôi cũng để ý rằng xu hướng sử dụng "sign in" đang tăng lên, đặc biệt là với các địch vụ phổ biến. Tuy nhiên Facebook thì vẫn trung thành với "log in".

![](http://blog.codinghorror.com/content/images/2015/01/log-in-vs-sign-in-graph.png)

## Hoạt động với trình quản lý mật khẩu của trình duyệt

Tất cả các hộp thoại đăng nhập bạn tạo ra nên được kiểm thử với các trình quản lý mật khẩu mặc định trên ...

- [Internet Explorer](http://windows.microsoft.com/en-us/internet-explorer/fill-in-forms-remember-passwords-autocomplete#ie=ie-11)
- [Chrome](https://support.google.com/chrome/answer/95606?hl=en)
- [Firefox](https://support.mozilla.org/en-US/kb/password-manager-remember-delete-change-passwords)
- [Safari](http://support.apple.com/en-us/HT204085)

Ít nhất, sau lần đăng nhập đầu tiên, username và mật khẩu nên được điền tự động ở những lần tiếp theo trên cùng trình duyệt.

![](http://blog.codinghorror.com/content/images/2015/01/log-in-autofill.png)

Người dùng dựa trên những trình quản lý mật khẩu có sẵn trong những trình duyệt họ dùng, và bất kỳ một hộp thoại đăng nhập tân tiến nào cũng nên tôn trọng điều này và thiết kế hợp cách. VD: trường mật khẩu nên có `type="password"` trong mã HTML với tên trường mà trình duyệt có thể nhận ra đó là một trường nhập mật khẩu.

Mặc dù có [LastPass](https://lastpass.com/) và các sản phẩm tương tự, tuy nhiên tôi giả định một cách chung chung rằng nếu hộp thoại đăng nhập hoạt động với các trình quản lý mật khẩu có sẵn của trình duyệt, nó sẽ hoạt động với các tiện ích của bên thứ 3.

## Xử lý các lỗi phổ biến của người dùng

Oops, người dùng nhập mật khẩu khi đang bật caps lock? Bạn nên báo cho họ biết việc này.

![](http://blog.codinghorror.com/content/images/2015/01/password-entry-caps-lock-is-on.png)

Oops, người dùng nhập email name@gmal.com thay vì name@gmail.com? Hay name@hotmail.cm thay vì name@hotmail.com? Bạn nên sửa những lỗi đánh máy trong các tên miền email thông dụng cho người dùng, hoặc thông báo cho họ biết về sai sót.

(Tôi cũng là một người ủng hộ nhiệt liệt cho ý tưởng [trình duyệt mặc nhiên hỗ trợ "hiển thị mật khẩu"](http://answers.microsoft.com/en-us/ie/wiki/ie11-iewindows8_1/the-use-of-the-password-reveal-eye-button-in/19a9dee2-fb0c-4c26-a6bc-ac02cf98d80e) cho trường mật khẩu để người dùng có thể xác nhận mật khẩu mà anh ấy/cô ấy đã nhập hoặc được tự động nhập đúng như mong muốn. Hiện chỉ có Internet Explorer và (*có thể*) Safari có tính năng này, nhưng tôi nghĩ tất cả các trình duyệt đều nên có.)

## Giúp người dùng chọn mật khẩu tốt hơn

Có rất nhiều các luồng ý kiến khác nhau về việc ~~ép buộc~~ giúp đỡ người dùng lựa chọn mật khẩu khác với những mật khẩu dở khôn tả như [password123 và iloveyou, v.v.](http://blog.codinghorror.com/dictionary-attacks-101/)

Chúng ta vẫn thường gặp những công cụ đo độ mạnh của mật khẩu cập nhật theo mỗi kí tự bạn nhập vào trường mật khẩu.

![](http://blog.codinghorror.com/content/images/2015/01/dropbox-password-strength-meters.png)

Đây là một ý tưởng thông minh, nhưng một vài trang web lại áp dụng giống như một màn thuyết giáo tệ hại và không phù hợp với thị hiếu của tôi. Việc thực hiện ý tưởng này cũng còn nhiều điều bỏ ngỏ, ví dụ như việc quyết định độ mạnh yếu của mật khẩu hoàn toàn phụ thuộc vào cảm hứng của người sở hữu (hoặc thiết kế) trang web. Một mật khẩu được coi là "tốt" trên trang này nhưng lại là "mật khẩu này chỉ dành cho các bé 3 tuổi" ở một trang khác. Một điều không dễ chịu chút nào.

Vì thế, ở Discourse, thay vì làm những thứ trên, tôi quyết định đặt mặc định một cách tuyệt đối rằng độ dài tối thiểu của mật khẩu phải là 8 kí tự, sau đó kiểm tra mật khẩu và bảo đảm rằng nó không nằm trong danh sách [10.000 mật khẩu thông dụng nhất](http://thepasswordproject.com/) bằng cách kiểm tra hash của mật khẩu.

![](http://blog.codinghorror.com/content/images/2015/01/create-new-account-password-too-common.png)

## Đừng quên bàn phím

Ở thời điểm hiện nay, tôi cảm thấy những người dùng bàn phím (vật lý) đang dần vắng bóng, nhưng cho những người trong chúng ta vẫn đang dùng và giữ thói quen gõ thật nhanh như dưới đây khi gặp hộp thoại đăng nhập

`name@example.com`, `tab`, `p4$$w0rd`, `enter`

... *làm ơn* chắc chắn rằng (hộp thoại đăng nhập) vẫn hoạt động phù hợp với thói quen trên. Tab để chuyển trường, Enter để gửi, v.v.

## Giới hạn số lượt trên tất cả mọi thứ

Bạn nên [giới hạn số lượt bất cứ việc gì mà người dùng có thể thực hiện, ở bất cứ đâu](http://blog.codinghorror.com/rate-limiting-and-velocity-checking/), và điều đó càng đúng đẵn với hộp thoại đăng nhập.

Nếu có người quên mật khẩu của mình và cố gắng đăng nhập 3 lần, hay gửi 3 yêu cầu quên mật khẩu, điều này là dễ hiểu. Nhưng sẽ hơi lạ nếu ai đó cố gắng đăng nhập hàng nghìn lần, hoặc gửi hàng ngàn yêu cầu quên mật khẩu. Tại sao, tôi thậm chí có thể phỏng đoán rằng những yêu cầu trên không phải đến từ ... con người.

![](http://blog.codinghorror.com/content/images/2015/01/too-many-failed-log-in-attempts.png)

Bạn có thể dùng vài kĩ thuật "lạ mắt" như tạm khóa tài khoản hay cho hiển thị CAPTCHA nếu có quá nhiều lần đăng nhập thất bại, nhưng việc này có thể dễ dàng khiến người dùng bực bội, khó chịu, vì thế hãy suy xét khi áp dụng.

Tôi suy nghĩ về một giải pháp đẹp và trung dung hơn; đó là thêm vào khoảng dừng giữa các lần thực hiện cùng một hành động, tăng thời gian dừng này lên theo số lần đăng nhập thất bại hay yêu cầu quên mật khẩu từ cùng 1 địa chỉ IP. Kĩ thuật này cũng đã được áp dụng vào Discourse.

## Những thứ tôi đã quên

Tôi đã cố gắng nhớ lại mọi thứ đã trải qua khi chúng tôi xây dựng hộp thoại đăng nhập hoàn hảo cho Discourse, nhưng tôi chắc chắn đã quên mất điều gì đó, hoặc có lẽ đã nhớ không được chi tiết. Hãy nhớ rằng [Discourse là mã nguồn mở 100%](https://github.com/discourse/discourse) và theo định nghĩa vẫn là một sản phẩm trong quá trình phát triển - nên theo cách nói ưa thích của bạn tôi, [Miguel de Icaza](http://tirania.org/blog/), thì khi sản phẩm đổ vỡ, bạn có thể giữ cả 2 nửa. Hãy thoải mái kiểm thử những thứ chúng tôi đã áp dụng và chia sẻ cho chúng tôi ý kiến của bạn ở phần bình luận, hoặc trỏ tới các ví dụ khác về các trải nghiệm đăng nhập tuyệt cú mèo, hay trích dẫn các lời khuyên hữu ích.

Việc đăng nhập chỉ gồm 1 biểu mẫu đơn giản với 2 trường, 1 liên kết và 2 nút. Nhưng sau khi đọc hết những điều trên, chắc chắn bạn sẽ đồng ý với tôi rằng đây là một vấn đề phức tạp, trái ngược với sự giản đơn bên ngoài. Và có lẽ, phương pháp tốt nhất là không xây dựng hộp thoại đăng nhập nào cả, mà dựa trên hệ thống xác thực bên ngoài bất cứ khi nào có thể.

Giống, như là, Chúa vậy.
