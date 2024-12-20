Mọi người đều bắt đầu từ đâu đó, kể cả các chuyên gia. Chương này chứa một số mẹo và gợi ý dành cho người mới bắt đầu lập trình Arduino. Arduino được phát triển dành cho những sinh viên đang bước vào lĩnh vực lập trình nhúng, cho phép họ bắt tay vào thực hiện mà không bị choáng ngợp bởi các chi tiết kỹ thuật. Bởi vì một số người đam mê và có sở thích Arduino có thể chưa được đào tạo về phần mềm chính thức, nên có một số điều đáng nói "nhân tiện" mà hầu hết những người thực hành dày dạn kinh nghiệm đều coi đó là điều hiển nhiên. 
##  Diễn đàn: Đầu tư công sức 
-   Diễn đàn thường xuyên chứa các bài đăng yêu cầu trợ giúp để phát triển một cái gì đó phức tạp. Yêu cầu thường ở dạng "Tôi muốn làm... Tôi là người mới - ai đó có thể giúp được không?" Việc không nhận thức được sự phức tạp không phải là một tội ác và là một người mới cũng không sao cả. Nhưng phải mất bao lâu để gõ yêu cầu này? Mười giây? Những người trả lời sẽ phải nỗ lực đến mức nào?  Có thể là mười giây nếu bạn nhận được phản hồi. 
-   Mọi người sẵn sàng giúp đỡ hơn nhiều nếu họ thấy bạn đã đầu tư công sức vào việc đó. Bạn đã đặt ra những gì bạn nghĩ là cần thiết và bạn nghĩ mình sẽ đạt được điều đó như thế nào chưa? Bạn có thể sai về điều đó vì điều đó chứng tỏ rằng bạn không chỉ ném vấn đề vào tường và hy vọng người khác sẽ làm tất cả công việc.
##  Bắt đầu nhỏ 
-   Đôi khi các yêu cầu được thực hiện để giúp lập trình các bài tập lớn và phức tạp. Phản hồi thông thường cho những bài đăng này là không trả lời gì cả. Không phải là không ai biết câu trả lời cho câu hỏi mà là không ai muốn bỏ công sức để hướng dẫn người dùng về nhiều điều cần phải học trước tiên. Nếu người dùng phải tiếp tục nhiệm vụ đó, hãy chia nó thành các phần nhỏ hơn. Sau đó đặt những câu hỏi cụ thể về những khó khăn đang thách thức.  
-   Tuy nhiên, cách tiếp cận tốt nhất là bắt đầu từ việc nhỏ với các bài tập đơn giản hơn. Mọi người đều biết điều này nhưng những người đam mê lại trở nên thiếu kiên nhẫn. Bạn là kiểu người chỉ muốn "câu trả lời" hay bạn muốn biết cách xác định câu trả lời? Kinh nghiệm là người thầy tốt nhất. 
-   Có lý do mà mọi người bắt đầu với đèn LED nhấp nháy. Đèn LED rất đơn giản - chúng bật hoặc tắt. Đơn giản như vậy nhưng vẫn có những bài học cần rút ra. Ví dụ, nếu đèn LED không sáng thì nguyên nhân là gì? Nếu bạn chưa từng gặp phải điều đó trước đây, bạn có thể không nhận ra rằng đèn LED được nối sai cực. Đừng lừa dối bản thân để thoát khỏi những khoảnh khắc tập luyện này.
##  Phương pháp tiếp cận hợp đồng chính phủ 
-   Các lập trình viên mới, được trang bị kiến ​​thức về ngôn ngữ lập trình, thường nhảy vào viết toàn bộ chương trình cùng một lúc và sau đó cố gắng gỡ lỗi nó. Tôi muốn gọi đây là cách tiếp cận theo hợp đồng của chính phủ. Sau khi được trang bị các yêu cầu, phần mềm sẽ được viết ra và sau đó được kiểm tra ở phần cuối. Các phiên sửa lỗi tiếp theo có thể tạo ra mức độ điên rồ. 
-   Đừng hiểu sai ý tôi – yêu cầu rất quan trọng. Khi các yêu cầu đến từ chính chúng ta (trong sở thích), chúng sẽ thay đổi thường xuyên. Hoặc nếu bạn đang phát triển thứ gì đó chỉ để giải trí, bạn thậm chí có thể không có yêu cầu chắc chắn . Đây chỉ là một số lý do để tránh mã hóa mọi thứ trước khi thử nghiệm. 
-   Lý do tốt nhất để tránh cách tiếp cận theo hợp đồng của chính phủ là việc gỡ lỗi khó khăn hơn trên các thiết bị nhúng. Có thể không có sẵn trình gỡ lỗi hoặc khả năng theo dõi của nó bị hạn chế. Ví dụ: bạn không thể thực hiện quy trình dịch vụ ngắt. Một cách tiếp cận tốt hơn là bắt đầu từ quy mô nhỏ và sử dụng các phương pháp tiếp cận shell và stub cơ bản.
##  Shell cơ bản 
-   Thay vì cố gắng viết toàn bộ ứng dụng trước khi gỡ lỗi, hãy viết một shell cơ bản trước. Trong phần vỏ chương trình này, hãy viết mã hàm setup() và loop() tối thiểu cho mã Arduino của bạn. Đặc biệt khi sử dụng dev board ESP32, hãy tận dụng kết nối USB to serial bằng Serial Monitor. Điều này sẽ đơn giản hóa chu trình phát triển và thử nghiệm của bạn. 
-   Shell đầu tiên có thể chỉ là "Hello from setup()" và "Hello from loop()" trong hàm loop(), như được minh họa trong Listing 15-1. Hãy nhớ rằng chương trình đầu tiên này không cần phải quá sang trọng. Bằng cách cố gắng nhiều như vậy ngay từ đầu, bạn chứng minh được một chu trình biên dịch đầy đủ, tải lên flash và chạy thử nghiệm. Lệnh gọi delay() ở dòng 4 cho phép thư viện ESP32 thiết lập liên kết nối tiếp USB trước khi chạy tiếp. Một phần của bằng chứng về khái niệm là chỉ thiết lập bằng chứng về liên kết nối tiếp gỡ lỗi với Serial Monitor.

        0001: // basicshell.ino 
        0002: 
        0003: void setup() { 
        0004: delay(2000); // Allow for serial setup 
        0005: printf("Hello from setup()\n"); 
        0006: } 
        0007: 
        0008: void loop() { 
        0009: printf("Hello from loop()\n"); 
        0010: delay(1000); 
        0011: } 
Listing 15-1. A sample basic starting shell of a program. 

##  Phương pháp Stub
-   Rõ ràng là bạn muốn ứng dụng của mình làm được nhiều việc hơn shell cơ bản đó. Bắt đầu xây dựng trên khung đó bằng cách thêm các hàm sơ khai (Listing 15-2). Các hàm init_oled() và init_gpio() chỉ là sơ khai cho những gì sẽ trở thành hàm khởi tạo cho các thiết bị OLED và GPIO.
-   Compile, flash và test những gì bạn có. Nó có chạy không? Đầu ra từ Listing 15-2 sẽ trông như thế này trong Serial Monitor:
      
        Hello from setup() 
        init_oled() called. 
        init_gpio() called. 
        Hello from loop() 
        Hello from loop() 
        Hello from loop() 
        ... 

-   Bước tiếp theo là mở rộng chức năng của các hàm sơ khai – khởi tạo thiết bị thực tế. Hãy tránh sự cám dỗ để làm tất cả và giữ cho phần bổ sung mã ở mức nhỏ và tăng dần. Điều này sẽ giúp bạn bớt đau đầu khi có vấn đề mới phát sinh. Thật đáng kinh ngạc khi ngay cả những bổ sung nhỏ, rõ ràng cũng có thể gây ra nhiều rắc rối đến vậy.

        0001: // stubs.ino 
        0002: 
        003: static void init_oled() { 
        0004: printf("init_oled() called.\n"); 
        0005: } 
        0006: 
        007: static void init_gpio() { 
        0008: printf("init_gpio() called.\n"); 
        0009: } 
        0010: 
        0011: void setup() { 
        0012: delay(2000); // Allow for serial setup 
        0013: printf("Hello from setup()\n"); 
        0014: init_oled(); 
        0015: init_gpio(); 
        0016: } 
        0017: 
        0018: void loop() { 
        0019: printf("Hello from loop()\n"); 
        0020: delay(1000); 
        0021: } 
Listing 15-2. The basic shell program expanded with stubs. 

##  Sơ đồ khối 
-   Các ứng dụng lớn hơn có thể được hưởng lợi từ sơ đồ khối để lập kế hoạch cho các tác vụ FreeRTOS cần thiết. Các hàm setup() và loop() bắt đầu từ "loopTask", được cung cấp theo mặc định. Nếu bạn không thích cách phân bổ ngăn xếp loopTask, bạn có thể xóa tác vụ đó bằng cách gọi ing vTaskDelete(nullptr) từ loop() hoặc từ bên trong setup(). Bạn cần thêm những nhiệm vụ gì? Liệu các quy trình ISR có cung cấp sự kiện cho bất kỳ ai trong số họ không? Vẽ các đường ở nơi có thể là hàng đợi tin nhắn. Có lẽ nên sử dụng các đường chấm chấm trong đó các sự kiện, ngữ nghĩa hoặc mutex có liên quan giữa các tác vụ. Nó không nhất thiết phải là một sơ đồ được UML phê duyệt – chỉ cần sử dụng các quy ước có ý nghĩa với bạn. 
-   Là một phần của việc khai triển ứng dụng của bạn, hãy tạo từng tác vụ ban đầu dưới dạng một hàm sơ khai. Tất cả những gì chức năng đó cần làm là thông báo sự bắt đầu của nó. Một tác vụ không được phép quay lại trong FreeRTOS, vì vậy, đối với mục đích sơ khai, tác vụ đó có thể xóa tác vụ của mình sau thông báo. Sau đó, bạn có thể điền vào nhiệm vụ bằng mã cuối cùng.
##  Lỗi 
-   Khi bạn xây dựng ứng dụng của mình từng phần một, bạn có thể bất ngờ gặp phải lỗi chương trình thuộc loại này hay loại khác. Điều này có thể gây khó chịu nhất trong một ứng dụng đã hoàn thiện. Nhưng vì bạn đang phát triển ứng dụng của mình bằng cách thêm từng phần mã vào một thời điểm nên bạn đã biết mã được thêm vào là gì. Lỗi có thể liên quan đến mã được thêm vào. Các tùy chọn trình biên dịch Arduino được sử dụng không cho phép trình biên dịch cảnh báo về mọi thứ cần thiết. Hoặc nó có thể là cách mà tệp tiêu đề hỗ trợ newlib printf() được xác định. Dù bằng cách nào, một ví dụ về mã có thể dẫn đến lỗi là: 

        printf("The name of the task is ‘%s’\n"); 

-   Xem vấn đề? Cần có một đối số chuỗi C sau chuỗi định dạng để đáp ứng mục định dạng "%s". Hàm printf() sẽ mong đợi nó và sẽ tiếp cận ngăn xếp để lấy nó. Nhưng giá trị nó tìm thấy có thể là rác hoặc nullptr và gây ra lỗi. Trình biên dịch biết về những vấn đề này nhưng những cảnh báo này không được báo cáo vì lý do nào đó. 
-   Một nguồn lỗi phổ biến khác là hết dung lượng ngăn xếp. Nếu bạn không thể xác định ngay nguyên nhân lỗi, hãy phân bổ thêm không gian ngăn xếp tác vụ cho tất cả các tác vụ đã thêm. Điều này có thể loại bỏ lỗi. Sau khi bạn hoàn tất việc kiểm tra, việc phân bổ ngăn xếp khác nhau có thể được giảm bớt hoàn toàn. 
-   Ngoài ra còn có vấn đề về vòng đời của đối tượng cần lưu ý. Bạn đã gửi con trỏ qua hàng đợi chưa? Xem phần Biết thời gian sử dụng bộ nhớ của bạn. Hay đối tượng C++ đã bị hủy khi một tác vụ khác cố truy cập vào nó?
##  Biết thời gian lưu trữ của bạn 
-   Khi bạn mới bắt đầu, dường như có rất nhiều điều để học hỏi. Đừng để điều đó làm bạn nản lòng mà hãy kiểm tra đoạn mã sau: 

        static char area1[25]; 
        void function foo() { 
         char area2[25]; 

Bộ nhớ cho mảng vùng 1 được tạo ở đâu? Có giống khu vực 2 không? Mảng vùng1 được tạo trong vùng SRAM được phân bổ vĩnh viễn cho mảng đó. Kho lưu trữ đó không bao giờ biến mất.
-   Tuy nhiên, bộ nhớ của vùng 2 thì khác vì nó được phân bổ trên ngăn xếp. Thời điểm hàm foo() trả về, bộ nhớ đó sẽ được giải phóng. Ví dụ: nếu bạn chuyển con trỏ đến khu vực 2 bằng hàng đợi tin nhắn, con trỏ đó sẽ không hợp lệ tại thời điểm foo() trả về . 
-   Nếu bạn muốn mảng array2 tồn tại sau khi foo() trả về, bạn có thể khai báo nó tĩnh trong hàm: 

        static char area1[25]; 
        void function foo() { 
         static char area2[25]; 

-   Bằng cách thêm từ khóa tĩnh vào khai báo của vùng2, chúng tôi đã chuyển phân bổ bộ nhớ của nó sang cùng vùng với vùng1 (tức là không có trên ngăn xếp). 
-   Lưu ý rằng mảng array1 cũng được khai báo bằng thuộc tính static, nhưng trong trường hợp đó, từ khóa static có nghĩa khác (khi được khai báo bên ngoài hàm). Ngoài hàm, từ khóa tĩnh chỉ có nghĩa là không gán ký hiệu bên ngoài cho nó ("area1"). Khai báo các biến này bằng tĩnh sẽ tránh được xung đột ở bước liên kết. 
##  Tránh dùng tên ngoài
-   Các hàm và mục lưu trữ chung chỉ được tham chiếu bởi tệp nguồn hiện tại của bạn có thể phải được khai báo static. Nếu không có từ khóa tĩnh, tên sẽ trở thành "extern" và có thể ảnh hưởng đến các liên kết khác trong thư viện. Trừ khi chức năng hoặc toàn cầu của bạn cần phải ở bên ngoài, hãy khai báo chúng là static. 
-   Mặt khác, các hàm setup() và loop() phải là các ký hiệu bên ngoài vì trình liên kết phải gọi chúng từ mô-đun khởi động ứng dụng. Là bên ngoài cho phép trình liên kết định vị và liên kết với chúng. 
##  Tận dụng phạm vi 
-   Cách thực hành tốt nhất về phần mềm nên áp dụng là giới hạn phạm vi của các thực thể để chúng không thể bị nhầm lẫn hoặc được tham chiếu từ những nơi không nên có. Việc khai báo mọi thứ trên toàn cầu sẽ thuận tiện cho các dự án nhỏ nhưng có thể trở thành vấn đề đau đầu đối với các ứng dụng lớn hơn. Tôi thích gọi đây là phong cách lập trình cao bồi. Các lập trình viên nhớ đến COBOL sẽ liên tưởng đến. 
-   Vấn đề với phong cách cao bồi là nếu bạn tìm thấy một lỗi trong đó một thứ gì đó đang được sử dụng/sửa đổi khi không nên như vậy thì việc cô lập sẽ trở nên khó khăn. Thay vào đó, khi các quy tắc phạm vi của ngôn ngữ được sử dụng, trình biên dịch sẽ cho bạn biết trước khi bạn đang cố truy cập một số thứ không nên truy cập. Quyền truy cập được phép sẽ được thực thi. 
-   Một cách để hạn chế phạm vi tiếp cận của các thẻ điều khiển FreeRTOS và các mục dữ liệu khác là chuyển chúng vào các tác vụ với tư cách là thành viên của cấu trúc. Ví dụ: nếu một tác vụ cần điều khiển cho hàng đợi và một mutex, thì hãy chuyển các mục này trong cấu trúc cho tác vụ tại thời điểm tạo tác vụ. Sau đó, chỉ có tác vụ sử dụng mới biết về các thẻ điều khiển này.
##  Nghỉ ngơi bộ não 
-   Khi nói đến trải nghiệm của con người, các nhà tâm lý học cho chúng ta biết rằng có ít nhất 16 loại tính cách khác nhau (Myers-Briggs). Nhưng tôi tin rằng hầu hết mọi người sẽ tiếp tục giải quyết một vấn đề sau khi họ đã từ bỏ việc suy nghĩ một cách có ý thức về nó. Vì vậy, khi bạn thấy mình mất kiên nhẫn trong một buổi sửa lỗi vào đêm khuya, hãy cho phép mình nghỉ ngơi một chút. 
-   Nó cũng có thể giúp bạn tránh khỏi những rủi ro không cần thiết, có thể dẫn đến kết cục là khói ma thuật. 
-   Một số có thể ngủ ngon lành, trong khi những người khác sẽ trằn trọc trong đêm. Nhưng tâm trí nghiền ngẫm các sự kiện trong ngày và xem xét tất cả các tình huống có thể xảy ra. Vào buổi sáng, vợ/chồng của bạn có thể phàn nàn về những tiếng lầm bầm thập lục phân trong giấc ngủ của bạn. Nhưng khi tỉnh dậy, bạn thường sẽ có một số ý tưởng mới để thử. Nếu đó là một vấn đề đặc biệt khó khăn, khoảnh khắc eureka có thể mất vài ngày để hình thành. Bạn sẽ chinh phục.
##  Sổ Ghi Chú 
-   Khi đầu bạn đập vào gối vào ban đêm, bạn có thể đột nhiên nhớ lại một hoặc hai điều mà bạn đã quên chú ý đến trong mã hoặc mạch điện. Một cuốn sổ ghi chú ở đầu giường có thể là một công cụ hỗ trợ trí nhớ hữu ích. Khi bạn còn trẻ, đầu óc bạn thông thoáng và việc ghi nhớ mọi thứ rất dễ dàng. Tuy nhiên, khi bạn già đi, cuộc sống trở nên đầy rẫy những phức tạp và rồi mọi thứ sẽ bắt đầu rơi vào tình trạng rạn nứt. Một cuốn sổ tay rất hữu ích để ghi lại những gì đã được thử hoặc cách bạn giải quyết một vấn đề. Buổi sáng thứ Hai tại nơi làm việc được hưởng lợi từ việc có thể tiếp tục công việc mà bạn đã dừng lại từ thứ Sáu trước đó. 
-   Trừ khi bạn sử dụng một kỹ thuật cụ thể thường xuyên, bạn sẽ cần phải tra cứu nó. Đây là một cách khác mà việc ghi chú rất hữu ích. Ghi lại những API đặc biệt, kỹ thuật C++ hoặc FreeRTOS mà bạn thấy hữu ích. Nếu bạn muốn sao chép và dán, hãy tranh thủ sử dụng các trang web như evernote .com. Đây có lợi thế là có thể tìm kiếm được bằng điện tử.
##  Yêu cầu giúp đỡ 
-Kể từ khi xuất hiện "mạng lưới len hoang dã", chúng ta có được sự trợ giúp của các diễn đàn và công cụ tìm kiếm, cho phép chúng ta "ngẩn ngơ" để được trợ giúp. Tìm kiếm trên web thường là bước đầu tiên hiệu quả để có câu trả lời hoặc manh mối ngay lập tức. Nhưng đừng tin những gì bạn đọc được – không phải mọi lời khuyên đều tốt. Tùy thuộc vào bản chất của vấn đề, bạn sẽ thường phát hiện ra rằng những người khác cũng gặp phải vấn đề tương tự. Trong trường hợp đó, bạn có thể nhận được một hoặc nhiều câu trả lời được đăng để xử lý . 
-Khi tiếp cận diễn đàn, hãy đặt những câu hỏi thông minh. Các bài đăng trên diễn đàn như "I2C của tôi không hoạt động, bạn có thể giúp được không?" thể hiện rất ít sự chủ động. Đây là một kiểu nỗ lực khác "ném vấn đề qua tường và hy vọng vào kết quả tốt nhất". Bạn có mang xe đến gara và nói với họ rằng xe của bạn bị hỏng không? Các bài đăng trên diễn đàn không cần phải chơi trò chơi hai mươi câu hỏi. 
Đăng truy vấn của bạn với một số thông tin cụ thể:
    • Bản chất chính xác của vấn đề (phần nào của I2C không "hoạt động") • Bạn đang làm việc với thiết bị I2C nào? 
    • Bạn đã thử những gì cho đến nay?
    • Có lẽ chi tiết cụ thể về bảng phát triển ESP32 của bạn. 
    • Nền tảng phát triển – Arduino hay ESP-IDF? 
    • Bạn đang sử dụng thư viện nào, nếu có? 
    • Bất kỳ điều kỳ lạ nào khác có thể quan sát được.
-   Tôi sẽ tránh đăng mã trên bài đăng đầu tiên nhưng hãy sử dụng khả năng phán đoán tốt nhất của bạn. Một số người đăng rất nhiều mã như thể điều này khiến nó dễ hiểu. Tôi tin rằng sẽ hiệu quả hơn nếu giải thích bản chất của vấn đề trước. Bạn luôn có thể đăng mã dưới dạng theo dõi. 
-   Khi đăng mã, không phải lúc nào cũng cần đăng hết (đặc biệt khi dài). Đôi khi chỉ cần đăng những gì có thể góp phần gây ra vấn đề. Trong ví dụ của chúng tôi, bạn chỉ có thể đăng các hàm mã I2C được sử dụng. 
-   Diễn đàn thường có cách đăng "code" vào tin nhắn (như [code] . . . [/code]). Hãy chắc chắn để tận dụng điều đó bất cứ khi nào có thể. Mặt khác, giữa phông chữ cân xứng và việc thiếu tôn trọng thụt lề, mã sẽ trở thành một mớ hỗn độn khủng khiếp khi đọc. Tôi ghét đọc mã thụt lề khủng khiếp. 
-   Việc mô tả chính xác vấn đề sẽ có tác dụng phụ hữu ích, cho dù trong bài đăng hay qua email – khi bạn mô tả xong vấn đề, bạn có thể đã nhận ra câu trả lời. Ngoài ra, khi làm việc với đồng nghiệp hoặc bạn học, chỉ cần giải thích vấn đề cho họ cũng có thể mang lại kết quả tương tự.
##  Chia để trị 
-   Học sinh mới có thể bị thách thức bởi một ứng dụng chiếm giữ . Làm thế nào để bạn cô lập phần mã chịu trách nhiệm? Lập trình viên dày dạn biết kỹ thuật phân chia và chinh phục. 
-   Khái niệm này đơn giản như trò chơi đoán số. Nếu bạn phải đoán một số mà tôi đang nghĩ đến trong khoảng từ 1 đến 10, và bạn đoán là 6 và tôi trả lời rằng số đó thấp hơn, thì bạn sẽ chia lại số đó với số đoán có lẽ là 3. Cuối cùng, bạn sẽ có thể đoán số bằng cách giảm phạm vi sau mỗi lần thử. Khi một chương trình bị treo, bạn chia nó thành hai nửa cho đến khi cô lập được vùng mã vi phạm. 
-   Có thể sử dụng các phương pháp khác nhau để chỉ báo - in ra Màn hình nối tiếp hoặc kích hoạt đèn LED. Đèn LED rất hữu ích cho việc theo dõi ISR ​​ở những nơi bạn không thể in tin nhắn. Nếu bạn có đủ GPIO, bạn thậm chí có thể sử dụng đèn LED hai màu để báo hiệu những thứ khác nhau. Ý tưởng là để chỉ ra rằng mã đã được thực thi tại các điểm quan tâm. Nếu bạn cần nhiều hơn từ đèn LED, bạn có thể nhấp nháy mã khi không ở ISR. Khi bạn đã thu hẹp vùng mã nơi xảy ra sự cố, bạn có thể xem xét kỹ mã nguyên nhân một cách cẩn thận hơn.
##  Lập trình cho câu trả lời 
-   Tôi đã từng thấy các lập trình viên ở nơi làm việc tranh cãi suốt nửa giờ đồng hồ về việc điều gì sẽ xảy ra khi điều này điều nọ xảy ra. Thậm chí sau đó, cuộc tranh cãi thường vẫn không được giải quyết. Toàn bộ vấn đề thường có thể được giải quyết bằng cách viết một chương trình đơn giản kéo dài một phút để kiểm tra giả thuyết. Tất nhiên, hãy sử dụng một số cảm nhận thông thường với những gì bạn đã quan sát được:
    • Hành vi được quan sát có được API hỗ trợ không? 
    • Hay hành vi này là do lạm dụng API hoặc khai thác lỗi? 
-   Nếu API có nguồn mở thì mã nguồn thường là câu trả lời cuối cùng. Thông thường, mã và nhận xét sẽ chỉ ra mục đích của các giao diện được ghi chép kém. Kết luận: đừng ngại viết mã vứt đi.
##  Tận dụng lệnh find 
-   Khi kiểm tra mã nguồn mở, bạn có thể tìm kiếm mã đó trực tuyến hoặc kiểm tra những gì bạn gặp phải trong hệ thống của mình. Việc xem xét mã đã cài đặt là điều quan trọng khi bạn cho rằng mình đã tìm thấy lỗi trong thư viện mà bạn đang sử dụng. Một trong những nhược điểm của Arduino là rất nhiều thứ được thực hiện ở hậu trường và vẫn bị ẩn đối với học sinh. Nếu bạn đang sử dụng hệ thống POSIX (Linux, FreeBSD hoặc MacOS, v.v.) thì lệnh find cực kỳ hữu ích. Người dùng Windows có thể cài đặt WSL (Hệ thống con Windows cho Linux) để thực hiện điều tương tự hoặc sử dụng phiên bản lệnh Windows. 
-   Dành thời gian để kết bạn với lệnh tìm kiếm. Nó mạnh mẽ và có vẻ khó khăn đối với người mới, nhưng không có gì bí ẩn lớn ở đó cả. Chỉ cần rất linh hoạt là có thể hấp thụ được sóng nhỏ. Lệnh find hỗ trợ vô số tùy chọn khiến nó có vẻ phức tạp. Hãy xem xét điều quan trọng và hữu ích nhất trong số này. Định dạng lệnh cơ bản tuân theo mẫu chung sau: 

       find [options] path1 path2 ... [expression] 

-   Các tùy chọn trong dòng lệnh dành cho người dùng nâng cao hơn và chúng ta có thể yên tâm bỏ qua chúng ở đây . Một hoặc nhiều tên đường dẫn là tên thư mục mà bạn muốn bắt đầu tìm kiếm. Để có được kết quả, trước đây cần phải chỉ định tùy chọn -print cho thành phần biểu thức nhưng với lệnh Gnu find, điều này hiện được giả định theo mặc định:

        $ find basicshell stubs -print 
or just: 
        $ find basicshell stubs 
        basicshell 
        basicshell/basicshell.ino 
        stubs 
        stubs/stubs.ino 

-   Với dạng lệnh trên, tất cả tên đường dẫn giảm dần từ tên thư mục đã cho sẽ được liệt kê. Điều này bao gồm các thư mục và tập tin. Hãy giới hạn đầu ra ở các tệp có tùy chọn loại với đối số "f" (biểu thị tệp): 

        $ find basicshell stubs -type f 
        basicshell/basicshell.ino 
        stubs/stubs.ino

-   Bây giờ đầu ra chỉ hiển thị tên đường dẫn tệp. Đầu ra này vẫn không hữu ích. Điều chúng ta cần làm là ra lệnh cho lệnh find thực hiện điều gì đó với những tên tệp này. Lệnh grep là một ứng cử viên tuyệt vời:

        $ find basicshell stubs -type f -exec grep ‘setup’ {} \; 
        void setup() { 
         delay(2000); // Allow for serial setup 
         printf("Hello from setup()\n"); 
        void setup() { 
         delay(2000); // Allow for serial setup 
         printf("Hello from setup()\n"); 

-   Chúng ta gần đến đích rồi, nhưng trước tiên, hãy giải thích một vài điều. Chúng tôi đã thêm tùy chọn tìm kiếm exec theo sau là tên của lệnh (grep) và một số cú pháp đặc biệt. Đối số 'setup' là biểu thức chính quy grep mà chúng tôi đang tìm kiếm (hoặc một chuỗi đơn giản). Nó thường cần được đặt trong dấu nháy đơn để ngăn shell làm hỏng nó . Đối số "{}" cho biết vị trí trên dòng lệnh truyền tên đường dẫn (đến grep). Cuối cùng là "\;" mã thông báo đánh dấu sự kết thúc của lệnh. Việc sau là cần thiết vì bạn có thể thêm nhiều tùy chọn tìm kiếm hơn nữa sau lệnh được cung cấp. 
-   Để hữu ích hơn nữa, chúng ta cần xem tên tệp nơi grep tìm thấy kết quả khớp. Trong một số trường hợp, bạn cũng có thể muốn biết số dòng nơi tìm thấy kết quả khớp. Cả hai điều này đều được grep đáp ứng bằng cách sử dụng tùy chọn H (hiển thị tên đường dẫn) và n (hiển thị số dòng):

        $ find basicshell stubs -type f -exec grep -Hn setup {} \; 
        basicshell/basicshell.ino:3:void setup() { 
        basicshell/basicshell.ino:4: delay(2000); // Allow for serial setup basicshell/basicshell.ino:5: printf("Hello from setup()\n"); 
        stubs/stubs.ino:11:void setup() { 
        stubs/stubs.ino:12: delay(2000); // Allow for serial setup 
        stubs/stubs.ino:13: printf("Hello from setup()\n"); 

-   Điều này bây giờ cung cấp tất cả các chi tiết mà bạn có thể muốn. 
-   Đôi khi, chúng tôi chỉ muốn tìm xem tệp tiêu đề được cài đặt ở đâu. Trong trường hợp này, chúng tôi không muốn grep tệp mà chỉ muốn xác định vị trí của tệp. Ví dụ: tệp tiêu đề cho thư viện Arduino nRF24L01 được cài đặt ở đâu? Tệp tiêu đề có tên RF24 .h. Lumen có thể sử dụng lệnh tìm sau trên iMac của cô ấy:

        $ find ~ -type f 2>/dev/null | grep ‘RF24.h’ 
        /Users/lumen/Documents/Arduino/libraries/RF24/RF24.h 
        /Users/lumen/Downloads/RF24-1.3.4/RF24.h 

-   Dấu ngã (~) đại diện cho thư mục chính (trong hầu hết các shell). Bạn cũng có thể chỉ định rõ ràng $HOME hoặc thư mục . Mệnh đề "2>/dev/null" chỉ được thêm vào để chặn các thông báo lỗi về các thư mục mà cô ấy thiếu quyền truy cập (điều này xảy ra rất nhiều trên 
đặc biệt hữu ích nếu bạn kết thúc việc tìm kiếm mọi thứ (bắt đầu bằng thư mục gốc "/") . Dành nhiều thời gian khi tìm kiếm từ root (chắc chắn là thời điểm pha cà phê). Kết quả tìm kiếm trong ví dụ trước được dẫn vào grep để nó chỉ báo cáo những kết quả đường dẫn có chuỗi RF24 .h trong đó. Việc tìm kiếm này cũng có thể được thực hiện bằng cách sử dụng tùy chọn tên của lệnh find:

        $ find ~ -type f -name ‘RF24.h’ 2>/dev/null 
        /Users/lumen/Documents/Arduino/libraries/RF24/RF24.h 
        /Users/lumen/Downloads/RF24-1.3.4/RF24.h 

-   Dù bằng cách nào, rõ ràng là trên iMac của Lumen, thư mục ~/Documents/Arduino/librar ies/RF24 chứa tệp tiêu đề RF24 .h (và các tệp liên quan). 
-   Tùy chọn tên cũng chấp nhận tìm kiếm tập tin trên toàn cầu. Để tìm kiếm tất cả các tệp tiêu đề, bạn có thể thử: 

        $ find ~ -type f -name ‘*.h’ 2>/dev/null 

-   Điều này chỉ là bề nổi – nó cung cấp một công cụ quá mạnh để có thể bỏ qua. Tận dụng nó
##  Thay đổi vô tận
Một số lập trình viên sẽ chỉ phát triển phần mềm của họ cho đến khi nó "có vẻ hoạt động". Một khi họ nhìn thấy kết quả mà họ mong đợi, họ cho rằng công việc của mình đã hoàn thành. Ngay lập tức rửa tay, họ đưa nó vào sản xuất chỉ để trả lại để sửa lỗi. Đôi khi lặp đi lặp lại như vậy. 
Đối với công việc theo sở thích, bạn có thể phản đối rằng điều này có thể chấp nhận được. Tuy nhiên, những người có cùng sở thích sẽ chia sẻ mã của họ. Bạn có muốn gây ra mã xấu hoặc gây lúng túng cho người khác không? Đặt một ví dụ xấu?  Không giống như mạch điện tử hàn, phần mềm có khả năng uốn dẻo vô cùng, vì vậy đừng ngại cải tiến nó. Phần mềm thường cần được đánh bóng. 
Hãy tự hỏi: 
    • Có cách nào tốt hơn để viết đơn đăng ký này không? 
     - Thay thế các thủ tục macro bằng các hàm nội tuyến? 
     - Sử dụng mẫu C++, cho mã chung? 
     - Việc sử dụng Thư viện mẫu chuẩn (STL) có cải thiện ứng dụng không? 
     - Có cách nào hiệu quả hơn để thực hiện một số thao tác không? 
    • Mã có dễ hiểu không? 
    • Dễ dàng duy trì hay mở rộng? 
    • Ứng dụng có dễ bị khai thác hoặc sử dụng sai mục đích không? Không có lỗi? 
    • Mã có tận dụng tốt các quy tắc xác định phạm vi C/C++ để hạn chế quyền truy cập vào các thẻ điều khiển và các tài nguyên khác trong chương trình  không? 
    • Có rò rỉ bộ nhớ không? 
    • Có điều kiện đua không? 
    • Có bị hỏng bộ nhớ trong một số điều kiện không?
-   Hãy tự hào về công việc của bạn và làm cho nó tốt nhất có thể. Nếu thực hiện đúng cách, một ngày nào đó nó có thể giúp ích cho bạn trong quá trình xin việc. Các kỹ sư luôn tìm cách hoàn thiện tay nghề của mình.
##  Làm quen với Bit 
-   Tôi thường nhăn mặt khi xuất hiện các macro như BIT(x), được thiết kế để đặt một bit cụ thể trong một từ. Là một lập trình viên, tôi thích xem biểu thức thực tế (1 << x) hơn là mac ro BIT(x) . Việc sử dụng macro đòi hỏi phải có sự tin tưởng rằng nó được triển khai theo cách bạn cho là như vậy. Tôi ghét giả định. Vâng, tôi có thể tra cứu định nghĩa vĩ mô, nhưng cuộc đời thật ngắn ngủi. Việc thiết lập có khó khăn đến mức cần phải thực hiện việc gián tiếp này không? Tôi khuyến khích tất cả những người mới bắt đầu thành thạo thao tác bit trong C/C++. Sự thận trọng duy nhất của tôi là lưu tâm đến thứ tự thực hiện các thao tác. Nhưng điều này có thể dễ dàng khắc phục bằng một số dấu ngoặc xung quanh biểu thức. 
-   Điều này dẫn đến việc dành thời gian để tìm hiểu mức độ ưu tiên của toán tử C và sự khác biệt giữa & và && . Nếu bạn không chắc chắn về những điều này thì hãy đầu tư vào bản thân. Hãy học thật kỹ để có thể áp dụng chúng suốt đời. Tôi bắt đầu sự nghiệp của mình với một biểu đồ nhỏ dán trên màn hình. Nó vô cùng hữu ích.
##  Hiệu quả 
-   Có vẻ như hầu hết các lập trình viên mới đều bắt đầu bị ám ảnh bởi tính hiệu quả. Đối với họ, việc viết mã phiên bản hiệu quả nhất của bài tập là một vinh dự. Đừng hiểu sai ý tôi – có một nơi dành cho tính hiệu quả, chẳng hạn như trong MPU, nơi nó phải xử lý việc mã hóa và giải mã video mà hầu như không có đủ tài nguyên để thực hiện việc đó. Tuy nhiên, nhìn chung nhu cầu không lớn như bạn nghĩ. 
-   Một lập trình viên Linux cấp dưới từng phàn nàn với tôi về việc truy vấn MySQL kém hiệu quả như thế nào khi anh ta làm việc trong một chương trình C++. Anh ấy đã dành nhiều thời gian để tìm cách giảm chi phí này hơn mức anh ấy có thể tiết kiệm được khi tối ưu hóa mã. Truy vấn chạy một lần hoặc nhiều nhất là vài lần mỗi ngày . Trong bức tranh lớn, hiệu quả của thành phần này là không liên quan. 
-   Khi bạn bắt tay vào thay đổi vì mục đích hiệu quả, hãy tự hỏi liệu điều đó có quan trọng trong bức tranh toàn cảnh hay không. Người dùng cuối có nhận thấy sự khác biệt không? Liệu nó có làm cho mã ứng dụng trở nên khó hiểu và dễ bảo trì hơn không? Mã sẽ an toàn hơn? Đã có lúc thời gian sử dụng máy tính rất có giá trị. Trong thế giới ngày nay, chi phí của người lập trình viên là nơi chứa đựng chi phí. Nếu tất cả những gì bạn đạt được là có thêm thời gian cho tác vụ nhàn rỗi của FreeRTOS, thì bạn đã đạt được điều gì?
##  Vẻ đẹp của mã nguồn
-   Khi tôi còn trẻ và trong bụng đầy lửa giận, tôi đã nhận được bài tập đầu tiên được đánh dấu từ giáo sư cho học kỳ đó với số điểm chưa đầy đủ. Tôi khá khó chịu vì chương trình hoạt động hoàn hảo. Vậy vấn đề là gì? Vấn đề là nó không đủ đẹp. 
-  Bây giờ tôi quên mất những chi tiết cụ thể về sắc đẹp, nhưng bài học vẫn còn trong tôi. Bạn có thể nói rằng bài học đã để lại cho tôi một vết sẹo tốt. Khi tôi phản đối lần đầu, anh ấy đã trả lời cả lớp rằng mã chỉ được viết một lần nhưng phải đọc nhiều lần. Nếu mã xấu hoặc lộn xộn, nó có thể khó bảo trì và sẽ ít người muốn thực hiện nhiệm vụ duy trì nó. Anh ấy đã động viên chúng tôi để làm cho mã dễ đọc và đẹp mắt . Điều này bao gồm mã có định dạng đẹp, nhận xét có định dạng đẹp nhưng không có quá nhiều nhận xét. Quá nhiều nhận xét có thể làm mờ mã và bị bỏ qua trong quá trình bảo trì chương trình.
##  Fritzing vs Sơ đồ 
-   Tôi tin rằng làm việc từ sơ đồ Fritzing là một cách làm không tốt. Một người muốn trở thành họa sĩ không tiếp tục vẽ những bức tranh vẽ theo số. Tuy nhiên đây chính xác là sơ đồ Fritzing. Giống như họa sĩ có sở thích vẽ theo số, nó có thể phù hợp với một số người chỉ muốn tái tạo công trình. Tuy nhiên, những người mong muốn theo đuổi sự nghiệp trong lĩnh vực này nên tránh nó. 
-   Mặt khác, các sơ đồ là sự thể hiện trực quan về mạch điện là gì. Họ cung cấp trong nháy mắt những gì một sơ đồ nối dây không thể làm được. Bạn có thể hấp thụ một mạch điện bằng cách nhìn vào một mớ dây điện không? Tôi khuyến khích những người đam mê dành thời gian để tìm hiểu các ký hiệu và quy ước sơ đồ. Tìm hiểu cách nối dây cho các dự án của bạn từ sơ đồ thay vì sơ đồ nối dây.
##  Thanh toán ngay hoặc thanh toán sau 
-   Dưới đây là một số lời khuyên chung dành cho sinh viên dự đoán nghề nghiệp trong lĩnh vực lập trình, cho dù đó là lĩnh vực điện toán nhúng hay lĩnh vực khác. Để phát triển sự nghiệp một cách lành mạnh, bạn sẽ bắt đầu với những nhiệm vụ cấp dưới và chuyển sang những nhiệm vụ cấp cao hơn khi tài năng của bạn phát triển. Hãy dành thời gian và kinh nghiệm để phát triển tài năng đó. Đừng quá tham vọng và vội vàng. 
-   Đã từng có một quảng cáo Midas Muffler cũ ở Bắc Mỹ vào những năm 1970 với nội dung "bạn có thể trả tiền cho tôi ngay bây giờ hoặc trả tiền cho tôi sau". Tin nhắn nói về việc bảo trì sớm. Sự nghiệp của bạn cũng cần được bảo trì sớm. Nếu bạn làm việc đó bây giờ, nó sẽ mang lại lợi ích cho sự nghiệp của bạn sau này. Đừng ngại dành thời gian và hy sinh trong những năm đầu đó.
##  Lập trình viên không thể thiếu 
-   Lời khuyên cuối cùng của tôi liên quan đến thái độ của nhân viên. Sau khi những năm đầu sự nghiệp trôi qua, một số lập trình viên chuyển sang chế độ "bảo đảm công việc". Họ sẽ xây dựng những hệ thống khó theo dõi và giữ thông tin cho riêng mình. Họ không thích chia sẻ với các nhân viên khác. Động lực cho việc này là trở thành một thứ không thể thiếu đối với công ty. 
-   Bạn không muốn trở thành một nhân viên không thể thiếu. Đồng nghiệp sẽ không thích bạn và đàn ông sẽ không chịu đựng được điều đó mãi mãi. Họ sẽ chịu đòn nếu cần thiết để phá vỡ sự phụ thuộc đó. Các công ty không muốn bị bắt làm con tin. 
-   Có một lý do khác để tránh xa những thứ không thể thiếu – bạn sẽ muốn chuyển sang những thử thách mới và bỏ lại các chức năng công việc cũ của mình (cho cấp dưới). Ban quản lý sẽ không giao cho bạn những thử thách mới và thú vị nếu bạn cần hỗ trợ những chức năng cũ đó. Nếu những thứ cũ đó quá khó để giao cho cấp dưới, thì có thể cấp dưới đó sẽ nhận được cơ hội mới đó thay cho bạn. Tại nơi làm việc, bạn muốn sẵn sàng đón nhận những thử thách mới.
##  Màn cuối cùng 
-   Bây giờ chúng ta đã đi đến màn cuối cùng – phần cuối của cuốn sách này. Nhưng đây không phải là kết thúc dành cho bạn vì bạn sẽ áp dụng những gì bạn đã thực hành và áp dụng các khái niệm FreeRTOS đó vào các ứng dụng của riêng bạn. Tôi hy vọng bạn thích cuộc hành trình này. Cảm ơn bạn đã cho phép tôi được hướng dẫn của bạn.