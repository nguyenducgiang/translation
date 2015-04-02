---
Author: Peter Norvig
Translator: Nguyễn Đức Giang
---

# Tự học lập trình trong 10 năm

> Đây là bản dịch bài viết [Teach Yourself Programming in Ten Years](http://norvig.com/21-days.html) của [Peter Norvig](http://norvig.com/) thực hiện bởi [Nguyễn Đức Giang](https://github.com/nguyenducgiang).

## Tại sao mọi người đều vội vã như vậy?

Bước vào một cửa hàng sách bất kì, bạn sẽ thấy làm thế nào để Tự học Java trong 24 giờ (Teach Yourself Java in 24 Hours) bên cạnh vô số những cuốn tương tự về tự học C, SQL, Ruby, thuật toán trong vài ngày, thậm chí vài giờ. Tìm kiếm nâng cao trên Amazon với [tiêu đề: teach, yourself, hours, since: 2000] trả về 512 cuốn sách dạng này. Trong số 10 cuốn hàng đầu, 9 cuốn là sách về lập trình (cuốn còn lại là về công việc sổ sách, kế toán). Các kết quả tương tự cũng được tìm thấy khi thay "teach yourself" (tự học) với "learn" (học) hoặc "hours" (giờ) với "days" (ngày).

Như vậy, hoặc là mọi người đang rất vội vã trong việc học lập trình, hoặc lập trình có vẻ như là một lĩnh vực vô cùng dễ học hơn bất cứ lĩnh vực nào khác. Felleisen và những cộng sự đã đề cập tới xu hướng này trong cuốn sách [How to Design Programs](http://www.ccs.neu.edu/home/matthias/HtDP2e/index.html) khi cho rằng "Lập trình dở thì rất dễ. Những thằng ngốc có thể học nó trong 21 ngày ngay cả khi chưa biết gì (về lập trình)". Abstruse Goose cũng vẽ [tranh biếm họa](http://abstrusegoose.com/249) về việc này.

Hãy cùng phân tích một tiêu đề sách như [Tự học C++ trong 24 giờ](http://www.amazon.com/Sams-Teach-Yourself-Hours-5th/dp/0672333317/ref=sr_1_6?s=books&ie=UTF8&qid=1412708443&sr=1-6&keywords=learn+c%2B%2B+days) (Teach Yourself C++ in 24 Hours) có ý nghĩa thế nào:

- **Tự học** (Teach yourself): Trong 24 giờ, bạn sẽ không có thời gian để viết một vài chương trình đáng kể và học từ những thành công cũng như thất bại trong quá trình xây dựng các chương trình đó. Bạn sẽ không có đủ thời gian để làm việc cùng một lập trình viên có kinh nghiệm và trải nghiệm thế giới của C++. Tóm lại, bạn không có nhiều thời gian để học. Vì thế cuốn sách chỉ tập trung vào các vấn đề chung chung một cách hời hợt thay vì hướng đến những hiểu biết sâu sắc. Như Alexander Pope nói: học ít (không phải ít học - ND) là một việc nguy hiểm.

- **C++**: Trong 24 giờ bạn có thể học một vài cú pháp của C++ (nếu bạn đã biết một ngôn ngữ khác), nhưng bạn không thể học nhiều về cách sử dụng ngôn ngữ này. Nói một cách ngắn gọn: giả sử bạn là một lập trình viên Basic, bạn có thể học cách viết chương trình với phong cách Basic sử dụng cú pháp C++, nhưng bạn không thể biết thế mạnh (và điểm yếu) thực sự của C++. Điều này có ý nghĩa gì? [Alan Perlis](http://www-pu.informatik.uni-tuebingen.de/users/klaeren/epigrams.html) từng nói: "Một ngôn ngữ không ảnh hưởng đến suy nghĩ của bạn về lập trình thì không đáng để biết". Có thể bạn phải học một chút về C++ (hoặc thường thấy hơn JavaScript hay Processing) bởi vì bạn cần tiếp xúc với một công cụ có sẵn để hoàn thành một việc cụ thể. Nhưng khi đó bạn không học về lập trình, bạn đang học để giải quyết công việc đó.

- **Trong 24 giờ**: rất tiếc, chỉ thế này là không đủ, câu trả lời nằm trong phần kế tiếp.

## Tự học lập trình trong 10 năm

Các nhà nghiên cứu ([Bloom(1985)](http://www.amazon.com/exec/obidos/ASIN/034531509X/), [Bryan & Harter (1899)](http://norvig.com/21-days.html#bh), [Hayes (1989)](http://www.amazon.com/exec/obidos/ASIN/0805803092), [Simmon & Chase (1973)](http://norvig.com/21-days.html#sc)) chỉ ra rằng cần khoảng 10 năm để xây dựng kĩ năng và hiểu biết ở mức độ chuyên gia về bất kì một lĩnh vực nào trong một danh sách các lĩnh vực bao gồm chơi cờ vua, soạn nhạc, vận hành điện tín, hội họa, chơi dương cầm, bơi lội, tennis, và nghiên cứu về neuropsychology hay topo học. Điểm quan trọng nhất là thực hành một cách có chủ đích: không đơn thuần là làm những việc lặp đi lặp lại mà thử thách bản thân với những vấn đề vượt qua năng lực hiện tại của mình, thử giải quyết nó và phân tích hiệu suất của mình trong và sau khi làm và sửa chữa các sai sót. Lặp lại quá trình này. Tiếp tục lặp lại. Không có đường tắt: ngay cả Mozart, thần đồng âm nhạc từ lúc 4 tuổi, nhưng phải 13 năm sau mới cho ra đời các tác phẩm âm nhạc có giá trị ở tầm thế giới. Ở một dòng nhạc khác, nhóm nhạc Beatles dường như đột ngột xuất hiện với một chuỗi các bản hit #1 và có mặt trong chương trình Ed Sullivan năm 1964. Tuy nhiên họ đã chơi nhạc từ trước đó rất lâu trong những câu lạc bộ nhỏ ở Liverpool và Hamburg từ năm 1957, và mặc dù thu hút đại chúng từ sớm, thành công lớn quan trọng đầu tiên của họ, Sgt. Peppers, được phát hành vào năm 1967. [Malcolm Gladwell](http://www.amazon.com/Outliers-Story-Success-Malcolm-Gladwell/dp/0316017922) đã phổ biến ý tưởng này nhưng tập trung vào con số 10.000 giờ hơn là 10 năm.

Có thể con số kì diệu là 10.000 giờ, không phải 10 năm. Hoặc có thể là một số liệu khác; Henri Cartier-Bresson (1908-2004) từng nói "10.000 tấm ảnh đầu tiên bạn chụp là tệ nhất". Kĩ năng và hiểu biết ở mức độ chuyên gia một cách chân chính có thể mất cả đời để xây dựng: Samuel Johnson (1709-1784) nói "Sự xuất sắc trong bất kì lĩnh vực nào chỉ có thể đạt được bằng sự lao động của cả đời người, không thể đạt được với cái giá rẻ hơn." và Chaucer (1340-1400) phàn nàn "đời người quá ngắn, việc học thì lại rất dài.". Hippocrates (c. 400BC) được biết tới với đoạn trích "ars longa, vita brevis", là một đoạn trong "Ars longa, vita brevis, occasio praeceps, experimentum periculosum, iudicium difficile" có thể được diễn dịch như sau "Cuộc đời thì ngắn, việc học thì dài, những cơ hội đang lướt qua, những trải nghiệm đầy nguy cơ, những phán đoán nhiều trắc trở.". Dĩ nhiên, không có một con số cụ thể nào là câu trả lời cho tất cả: cho rằng mỗi một kĩ năng như lập trình, chơi cờ vua, chơi cờ đam hay soạn nhạc yêu cầu một số lượng thời gian như nhau để nắm vững là không hợp lý. Việc cho rằng tất cả mọi người cũng cần một khoảng thời gian như nhau cũng vậy.

## Bạn muốn trở thành lập trình viên?

Đây là công thức thành công của tôi cho việc lập trình:

- **Yêu thích** lập trình và làm bởi vì nó thú vị. Hãy chắc rằng công việc lập trình luôn luôn đủ thú vị để bạn có thể sẵn sàng bỏ 10 năm/10.000 giờ vào.

- **Lập trình** Cách tốt nhất để học là [thực hành](http://www.engines4ed.org/hyperbook/nodes/NODE-120-pg.html) (vừa học vừa làm). Cụ thể hơn, "hiệu suất tối đa cho các cá nhân trong một lĩnh vực cụ thể không được xác định như là một phần của việc nhiều kinh nghiệm, mà mức độ hiệu suất này có thể được nâng lên ngay cả bởi các cá nhân giàu kinh nghiệm như là kết quả của những nỗ lực có chủ đích." [(tr. 336)](http://www2.umassd.edu/swpi/DesignInCS/expertise.html) và "cách học tập hiệu quả nhất yêu cầu một tác vụ rõ ràng với độ khó phù hợp cho cá nhân được giao, phản hồi hữu ích, và cơ hội để lặp lại và sửa chữa lỗi." (tr. 20-21) Cuốn sách [Cognition in Practice: Mind, Mathematics, and Culture in Everyday Life](http://www.amazon.com/exec/obidos/ASIN/0521357349) là tài liệu tham khảo khá thú vị cho quan điểm này.

- **Trò chuyện** với các lập trình viên khác; đọc mã nguồn các chương trình khác. Điều này quan trọng hơn bất cứ cuốn sách hay khóa học nào.

- Nếu bạn muốn, hãy bỏ ra 4 năm học **đại học** (hoặc hơn ở trường cao học). Việc này sẽ tạo điều kiện cho bạn đến với các công việc yêu cầu bằng cấp cũng như các hiểu biết sâu sắc hơn về lĩnh vực bạn theo học. Nhưng nếu không thích học, bạn có thể (với một chút tâm huyết) giành được những trải nghiệm tương tự một cách tự thân hoặc từ công việc. Trong mọi trường hợp, chỉ học từ sách không là không đủ. "Việc đào tạo khoa học máy tính không thể khiến bất cứ ai trở thành một chuyên gia lập trình, nó cũng tương tự như việc học về bút lông và thuốc màu không thể làm bạn trở thành họa sĩ được" - Eric Raymond, tác giả  *The New Hacker's Dictionary*. Một trong những lập trình viên tốt nhất tôi từng thuê chỉ tốt nghiệp cấp III; cậu ấy đã tạo ra rất nhiều [phần mềm](http://www.mozilla.org/) [tuyệt vời](http://www.xemacs.org/), có [nhóm hâm mộ](http://groups.google.com/groups?q=alt.fan.jwz&meta=site%3Dgroups), và kiếm đủ tiền từ cổ phiếu để mua [hộp đêm](http://en.wikipedia.org/wiki/DNA_Lounge) cho mình.

- Làm việc trong **các dự án với** các lập trình viên khác. Hãy là lập trình viên xuất sắc nhất trong một số dự án; hãy là lập trình viên dở nhất trong một số dự án khác. Khi bạn là người xuất sắc nhất, bạn có dịp kiểm tra khả năng dẫn dắt dự án cũng như truyền cảm hứng cho những người khác với tầm nhìn của mình. Khi bạn là người dở nhất, bạn học được cách các chuyên gia làm việc, và những gì họ không muốn làm (vì họ sẽ yêu cầu bạn làm những việc đấy cho họ).

- Làm việc trên các **dự án kế thừa** từ các lập trình viên khác. Hiểu các chương trình được viết bởi lập trình viên khác. Tìm hiểu xem cần những gì để hiểu và làm việc với chương trình đó khi các lập trình viên tạo ra nó không có mặt. Suy nghĩ về việc thiết kế chương trình để công việc bảo trì của những người kế thừa (chương trình) từ bạn dễ dàng hơn.

- Học ít nhất nửa tá **ngôn ngữ lập trình**. Bao gồm 1 ngôn ngữ chú trọng vào lớp-trừu-tượng (class abstractions) (như Java hay C++), 1 ngôn ngữ chú trọng hàm-trừu-tượng (functional abstraction) (như Lisp hay ML hay Haskell), 1 ngôn ngữ hỗ trợ cú-pháp-trừu-tượng (như Lisp), 1 ngôn ngữ khai báo (như Prolog hay C++ templates), và 1 ngôn ngữ chú trọng tính song song (như Clojure hoặc Go).

- Hãy nhớ rằng có **"máy tính"** trong cụm từ "khoa học máy tính". Biết rõ máy tính của mình - thực hiện một chỉ dẫn, tìm nạp một từ từ bộ nhớ (khi có hoặc không có cache miss), đọc các từ liên tiếp từ đĩa hay tìm một đia chỉ mới trên đĩa - hết bao lâu. [Đáp án](#-p-n)

- Tham gia vào nỗ lực **tiêu chuẩn hóa** ngôn ngữ. Có thể là ủy ban ANSI C++, hoặc là việc quyết định xem phong cách viết mã ở khu vực của bạn nên dùng 2 hay 4 khoảng trắng cho việc lùi đầu dòng (indentation). Trong cả hai trường hợp, bạn sẽ biết được những người khác thích gì ở một ngôn ngữ, cảm nhận của họ sâu sắc thế nào, và có thể một chút về lí do học cảm thấy như vậy.

- Có ý thức về việc **thoát khỏi** nỗ lực tiêu chuẩn hóa ngôn ngữ càng nhanh càng tốt.

Cân nhắc tất cả các điểm trên, việc bạn có thể đi bao xa khi chỉ học từ sách còn là một nghi vấn. Trước khi đứa con đầu tiên chào đời, tôi đã đọc hết những cuốn sách *Làm thế nào để ...*, và vẫn cảm thấy như một kẻ mới vào nghề mù tịt. Nhiều tháng sau đó, khi đứa con thứ hai ra đời, liệu tôi có quay lại đọc những cuốn sách kia để ôn lại? Không. Thay vào đó tôi dựa vào những kinh nghiệm cá nhân, mà hóa ra lại hữu ích và làm tôi yên tâm hơn rất nhiều so với hàng ngàn trang sách được viết bởi các chuyên gia.

Fred Brooks, trong tiểu luận [No Silver Bullet](http://en.wikipedia.org/wiki/No_Silver_Bullet) (Không có viên đạn bạc nào cả) của mình đã đưa ra một kế hoạch gồm 3 bước để tìm kiếm các nhà thiết kế phần mềm xuất sắc:

1. Nhận diện một cách có hệ thống những nhà thiết kế hàng đầu càng sớm càng tốt.

2. Phân công một cố vấn nghề nghiệp chịu trách nhiệm cho sự phát triển của những nhà thiết kế tiềm năng và lưu giữ cẩn thận hồ sơ sự nghiệp.

3. Tạo cơ hội cho những nhà thiết kế đang phát triển này giao lưu và thúc đẩy lẫn nhau.

Những điều này dựa trên giả định rằng một số người có sẵn đủ những phẩm chất cần thiết để trở thành một nhà thiết kế xuất sắc; công việc là để cho họ đi đúng hướng. [Alan Perlis](http://www-pu.informatik.uni-tuebingen.de/users/klaeren/epigrams.html) trình bày súc tích hơn: "Mọi người đều có thể được dạy để điêu khắc: còn Michelangelo phải được dạy làm thể nào để không (điêu khắc). Với các lập trình viên xuất sắc cũng vậy". Perlis cho rằng những người xuất sắc có sẵn một vài tố chất vượt qua những thứ được đào tạo. Nhưng những tố chất đó đến từ đâu? Là do bẩm sinh? Hay do họ tích lũy qua sự chuyên cần? Như Auguste Gusteau (nhân vật đầu bếp giả tưởng trong phim hoạt hình Ratatouille) khẳng định "bất cứ ai cũng có thể nấu ăn, nhưng chỉ những người gan dạ mới có thể trở thành (đầu bếp) tuyệt vời." Tôi cho rằng đó sự sẵn sàng dành trọn một phần lớn của cuộc đời để thực hành. Nhưng có thể *gan dạ* là một cách để môt tả điều đó. Hoặc như người phê bình Gusteau, Anton Ego, nói: "Không phải ai cũng có thể trở thành nghệ sĩ xuất sắc, nhưng nghệ sĩ xuất sắc thì có thể xuất hiện ở bất cứ đâu."

Vì thế, đi mua những cuốn sách (tự học) Java/Ruby/JavaScript/PHP, bạn có thể thấy chút hữu dụng. Nhưng bạn không thể thay đổi cuộc đời mình, cũng như trình độ lập trình thực tế của bạn trong 24 giờ hay 21 ngày. Thế nếu nỗ lực chăm chỉ trong 24 tháng thì sao? Đến đây, bạn đã có thể bắt đầu hành trình của mình đến một nơi nào đó...

## Tài liệu tham khảo

Bloom, Benjamin (ed.) [Developing Talent in Young People](http://www.amazon.com/exec/obidos/ASIN/034531509X), Ballantine, 1985.

Brooks, Fred, [No Silver Bullets](http://citeseer.nj.nec.com/context/7718/0), IEEE Computer, vol. 20, no. 4, 1987, p. 10-19.

Bryan, W.L. & Harter, N. "Studies on the telegraphic language: The acquisition of a hierarchy of habits. Psychology Review, 1899, 8, 345-375

Hayes, John R., [Complete Problem Solver](http://www.amazon.com/exec/obidos/ASIN/0805803092) Lawrence Erlbaum, 1989.

Chase, William G. & Simon, Herbert A. ["Perception in Chess"](http://books.google.com/books?id=dYPSHAAACAAJ&dq=%22perception+in+chess%22+simon&ei=z4PyR5iIAZnmtQPbyLyuDQ) Cognitive Psychology, 1973, 4, 55-81.

Lave, Jean, [Cognition in Practice: Mind, Mathematics, and Culture in Everyday Life](http://www.amazon.com/exec/obidos/ASIN/0521357349), Cambridge University Press, 1988.

## Đáp án

Thời gian gần đúng cho một số hoạt động trên một PC điển hình:

Operation                           | Time (approx))
-------------------------------|--------------------------------------
execute typical instruction | 1/1,000,000,000 sec = 1 nanosec
fetch from L1 cache memory | 0.5 nanosec
branch misprediction |	5 nanosec
fetch from L2 cache memory | 7 nanosec
Mutex lock/unlock	| 25 nanosec
fetch from main memory | 100 nanosec
send 2K bytes over 1Gbps network |	20,000 nanosec
read 1MB sequentially from memory |	250,000 nanosec
fetch from new disk location (seek) |	8,000,000 nanosec
read 1MB sequentially from disk |	20,000,000 nanosec
send packet US to Europe and back |	150 milliseconds = 150,000,000 nanosec

## Phụ lục: Lựa chọn ngôn ngữ

Một vài người muốn hỏi về ngôn ngữ đầu tiên họ nên học. Không có đáp án duy nhất cho vấn đề này nhưng nên cân nhắc những điểm sau:

- *Sử dụng (như) bạn bè của mình*. Khi được hỏi "tôi nên dùng hệ điều hành nào, Windows, Unix hay Mac?", tôi thường trả lời: "sử dụng cái mà bạn bè của anh/chị đang dùng ấy." Điều này sẽ làm cho việc học hỏi từ bạn bè thuận lợi hơn khi bạn không gặp phải các rắc rối do sự khác biệt về hệ điều hay hay ngôn ngữ lập trình. Bạn cũng nên cân nhắc về những người bạn trong tương lai: bạn sẽ trở thành một phần của cộng đồng các lập trình viên (của ngôn ngữ bạn chọn) nếu bạn tiếp tục với lựa chọn của mình. Ngôn ngữ bạn chọn có cộng đồng lớn, đang phát triển mạnh mẽ hay là một cộng đồng nhỏ đang lụi tàn? Có đủ các nguồn sách, web site và diễn đàn trực tuyến để bạn tìm kiếm các câu trả lời? Bạn có thích những người ở cộng đồng đó?

- *Tính giản đơn*. Ngôn ngữ lập trình như C++ hay Java được thiết kế cho các đội ngũ với nhiều lập trình viên giàu kinh nghiệm, phát triển các sản phẩm chuyên nghiệp, nơi mà hiệu quả chạy (run-time) của mã (code) được quan tâm. Vì vậy, các ngôn ngữ này bao gồm những phần phức tạp được thiết kế để giải quyết vấn đề trên. Bạn đang quan tâm đến việc học lập trình. Bạn không cần những thứ phức tạp như vậy. Bạn cần một ngôn ngữ được thiết kế để dễ học và ghi nhớ bởi một lập trình viên mới.

- *Học mà chơi*. Bạn thích dùng cách nào để học dương cầm: cách thông thường, hướng tới tương tác, tức là bạn sẽ nghe thấy nốt nhạc ngay sau khi bạn nhấn phím; hay theo chế độ "batch", bạn sẽ chỉ nghe thấy âm thanh sau khi hoàn thành cả bản nhạc? Rõ ràng tương tác làm cho việc học dương cầm dễ dàng hơn, với lập trình cũng vậy. Hãy lựa chọn một ngôn ngữ có chế độ tương tác để bắt đầu.

Từ những tiêu chí trên, lời khuyên của tôi cho ngôn ngữ lập trình đầu tiên là [Python](http://python.org/) và [Scheme](http://www.schemers.org/). Một lựa chọn khác là JavaScript, không phải vì nó được thiết kế phù hợp cho những người mới bắt đầu, mà bởi vì nó có rất nhiều hướng dẫn trên mạng, chẳng hạn trên [Khan Academy](https://www.khanacademy.org/computing/cs/programming). Tuy nhiên, phụ thuộc vào hoàn cảnh cụ thể của bạn, có thể sẽ có những lựa chọn khác phù hợp hơn. Nếu số tuổi của bạn vẫn còn là 1 chữ số, có thể bạn sẽ thích [Alice](http://alice.org/), [Squeak](http://www.squeak.org/) hay [Blockly](https://blockly-demo.appspot.com/static/apps/index.html) (các bạn lớn tuổi hơn có thể cũng sẽ thích những thứ này). Điều quan trọng nhất là bạn lựa chọn và bắt đầu học.

## Phụ lục: Sách và các tài nguyên khác

Vài người hỏi tôi về những cuốn sách và trang web để học (lập trình). Tôi xin phép lặp lại rằng "chỉ học từ sách không là không đủ", tuy nhiên tôi có thể giới thiệu một số tài liệu như sau:

- **Scheme:** [Structure and Interpretation of Computer Programs (Abelson & Sussman)](http://www.amazon.com/gp/product/0262011530) có lẽ là tài liệu giới thiệu tốt nhất về khoa học máy tính, nó cũng dạy cả lập trình như là một phương thức để hiểu về khoa học máy tính. Bạn có thể xem trực tuyến [các video bài giảng](http://www.swiss.ai.mit.edu/classes/6.001/abelson-sussman-lectures/) của cuốn sách này cũng như đọc [toàn bộ nội dung](http://mitpress.mit.edu/sicp/full-text/book/book.html) của cuốn sách. Cuốn sách này là một thử thách và có thể loại bỏ một số người mà có thể họ sẽ thành công hơn với một cách tiếp cận khác.

- **Scheme:** [How to Design Programs (Felleisen và cộng sự)](http://www.amazon.com/gp/product/0262062186) là một trong những cuốn sách tốt nhất về cách thiết kế chương trình thực sự theo lối thanh nhã và phiếm-hàm-cách (functional way).

- **Python:** [Python Programming: An Intro to CS (Zelle)](http://www.amazon.com/gp/product/1887902996), một cuốn sách khá tốt giới thiệu về Python.

- **Python:** Một số [hướng dẫn](http://wiki.python.org/moin/BeginnersGuide) trực tuyến có sẵn trên [Python.org](http://python.org/).

- **Oz:** [Concepts, Techniques, and Models of Computer Programming (Van Roy & Haridi)](http://www.amazon.com/gp/product/0262220695) được một số người xem như là sự kế thừa từ Abelson & Sussman. Cuốn sách sẽ đưa bạn du hành qua các ý tưởng lớn về lập trình, phạm vi đề cập rộng hơn Abelson & Sussman trong khi dễ đọc và thực hành hơn. Cuốn sách sử dụng Oz, một ngôn ngữ ít được biết đến, nhưng có tác dụng làm cơ sở để học các ngôn ngữ khác.

## Ghi chú

T. Capey phát hiện ra trang [Complete Problem Solver](http://www.amazon.com/exec/obidos/ASIN/0805803092) trên Amazon hiện tại có cuốn "Teach Yourself Bengali in 21 days" và "Teach Yourself Grammar and Style" trong phần "Khách hàng mua sản phẩm này cũng mua những sản phẩm dưới đây". Tôi đoán một phần lớn những người vào xem cuốn đó truy cập từ trang này (http://norvig.com/21-days.html, trang gốc của bài viết - ND). Xin gửi lời cảm ơn tới Ross Cohen vì sự giúp đỡ cho phần về Hippocrates.
