# Quy tắc thiết kế thẻ Anki

Bài viết được dịch từ bài [Rules for Designing Precise Anki Cards](https://controlaltbackspace.org/precise/). Các thẻ ví dụ trong bài viết đã được chỉnh sửa nội dung để phù hợp với phần lớn người đọc (Các ví dụ gốc được làm cho dân Khoa học máy tính nên các thuật ngữ sẽ tương đối khó hiểu).

##

Việc ôn tập trong Anki rất dễ dàng:
tất cả những gì bạn phải làm là trả lời câu hỏi
và nhấn nút để cho biết bạn nhớ câu hỏi đó tốt như thế nào.
Tuy nhiên, việc tạo thẻ để ôn tập
là một quá trình phức tạp, vừa là nghệ thuật vừa là khoa học,
và việc bạn thiết kế thẻ tốt như thế nào
có thể tạo nên sự khác biệt giữa
các buổi học dễ dàng dẫn đến việc học hiệu quả
và các buổi học gây nản lòng dẫn đến việc học tầm thường.
Do đó, thiết kế thẻ là kỹ năng cơ bản nhất của việc sử dụng phương pháp lặp lại cách quãng,
và bạn nên dành thời gian để học cách thực hiện tốt.

Trong một vài bài đăng tiếp theo về việc tạo thẻ cho các hệ thống lặp lại cách quãng,
tôi sẽ thường xuyên tham khảo
[Hai mươi quy tắc xây dựng kiến ​​thức] của SuperMemo (http://super-memory.com/articles/20rules.htm).
Sẽ rất khó để nói quá về tầm quan trọng và ảnh hưởng của tài liệu này
trong cộng đồng lặp lại ngắt quãng,
và nếu bạn chưa đọc, bạn nên đọc ngay bây giờ,
hoặc ít nhất là đưa nó vào danh sách đọc của bạn.
Trên thực tế, bạn nên đọc nó hai lần,
cân nhắc việc ghi nhớ các nguyên tắc,
và tiếp tục quay lại và đọc lại khi bạn tìm hiểu thêm về lặp lại ngắt quãng –
đó là một trong những nguồn tài nguyên mà bạn học được nhiều hơn mỗi lần đọc nó.

## Tầm quan trọng của việc đặt câu hỏi đúng

SRS thực hiện công việc tuyệt vời là giúp bạn nhớ
thông tin bạn đưa vào đó.
Tuy nhiên, đây là một công cụ rác vào, rác ra mạnh mẽ:
nếu bạn đưa vào tài liệu
không hữu ích hoặc không kiểm tra những điều bạn muốn biết,
bạn sẽ nhớ nó,
nhưng nó sẽ không giúp ích gì cho bạn; bạn sẽ chỉ lãng phí thời gian vào việc đánh giá.
Điều này đặt ra một thách thức cho người dùng,
bởi vì những thay đổi nhỏ trong cách bạn đặt câu hỏi
có thể khiến nó không kiểm tra được điều bạn muốn.
SRS khá giống với thần đèn trong câu tục ngữ:
hãy mô tả điều bạn muốn nhận theo cách sai,
và thần đèn sẽ diễn giải mong muốn của bạn theo cách lố bịch nhất có thể
và bạn sẽ học được điều gì đó không có ích thực tế.
Ví dụ, gần đây tôi đã tìm thấy một thẻ có khoảng thời gian vài năm
trong bộ sưu tập của riêng tôi,
hỏi tùy chọn nào cho lệnh Unix `cp` (sao chép)
khiến nó yêu cầu xác nhận
trước khi ghi đè lên các tệp hiện có.
Tôi đã trả lời dễ dàng và chính xác, “ `cp -i`,”
nhưng khi đưa ra câu trả lời đó, tôi nhận ra rằng tôi đã hoàn toàn quên
rằng `cp` _có_ một tùy chọn như vậy ngay từ đầu,
nên tôi sẽ không bao giờ nghĩ đến việc sử dụng tùy chọn
khi nó hữu ích,
và thông tin này hầu như vô giá trị đối với tôi.
Trong những trường hợp khác, bạn có thể ghi nhớ một lỗi ngữ pháp trên thẻ của mình,
hoặc một câu trả lời đã học được cho một lời nhắc
mà bạn sẽ không bao giờ gặp phải trong cuộc sống thực.

Nói cách khác, các câu hỏi SRS dễ bị _quá khớp_.
[Quá khớp](https://en.wikipedia.org/wiki/Overfitting), trong mô hình thống kê và học máy,
xảy ra khi một mô hình trở nên "quá tốt"
trong việc dự đoán dữ liệu mà bạn đào tạo nó –
nó bắt đầu coi nhiễu ngẫu nhiên có trong dữ liệu đào tạo
là một nguồn dự đoán có ý nghĩa.
Tất nhiên, nhiễu ngẫu nhiên không biểu thị bất kỳ mối quan hệ có ý nghĩa nào
có thể hữu ích trong việc dự đoán thông tin mới.
Do đó, quá khớp cải thiện tỷ lệ chính xác của mô hình trên dữ liệu đào tạo
nhưng lại làm giảm tỷ lệ này khi áp dụng cho dữ liệu mới,
tức là một tình huống thực tế.
Trong bối cảnh lặp lại theo khoảng cách,
vì SRS rất tốt trong việc giúp bạn học mọi thứ một cách hiệu quả,
nó sẽ tối ưu hóa trí nhớ của bạn về hầu hết mọi thứ,
nhưng nếu bạn không diễn đạt câu hỏi của mình một cách chính xác,
nó sẽ giúp bạn nhớ thông tin không liên quan hoặc nhiễu ngẫu nhiên,
thay vì thông tin mà bạn thực sự muốn biết.


Để tránh việc quá khớp, quy tắc số một khi thêm thẻ là:
mỗi khi bạn bắt gặp điều gì đó mà bạn nghĩ mình muốn nhớ,
**xác định chính xác điều bạn muốn biết**,
và càng chính xác càng tốt.
Sau đó, và chỉ sau đó,
hãy tạo một hoặc nhiều thẻ hỏi về chính xác điều đó và không hỏi gì khác.
Làm như vậy khó hơn và khiến quá trình học ban đầu của bạn dài hơn,
so với việc chỉ đổ thông tin vào thẻ ghi nhớ,
nhưng hiệu quả hơn nhiều!
Ngoài ra, quá trình này giúp bạn hiểu và ghi nhớ thông tin,
thậm chí trước khi bạn bắt đầu xem lại các thẻ:
bạn buộc phải suy nghĩ về ý nghĩa chính xác của thông tin đối với bạn,
khi nào bạn cần sử dụng thông tin đó,
và thông tin đó liên quan như thế nào đến những điều bạn đã biết.
Đây là một dạng kỹ thuật ghi nhớ ngẫu nhiên được gọi là _mã hóa chi tiết_,
luôn được phát hiện là
một trong những cách hiệu quả nhất để học mọi thứ
– và bạn nhận được nó miễn phí
trong khi làm một việc mà bạn đã cần làm để tạo thẻ ghi nhớ của mình!

Phần còn lại của bài đăng này sẽ nêu ra một số quy tắc
để giúp bạn đặt câu hỏi đúng trên thẻ của mình.
Mặc dù tôi đã đưa ra một hoặc hai ví dụ,
phần lớn trong số chúng là thẻ thực tế
được lấy ra từ bộ sưu tập cá nhân của tôi ngày hôm nay,
chỉ để chứng minh rằng hầu hết mọi người dùng lặp lại cách quãng
đều có một số bộ xương này trong tủ của mình
(nhiều bộ xương trong số chúng nằm trên thẻ cũ của tôi, nhưng một số bộ xương mới hơn nhiều).

## Câu hỏi chỉ nên hỏi chính xác một điều

Quy tắc số 4 của [Hai mươi quy tắc](http://super-memory.com/articles/20rules.htm) gọi đây là _Nguyên tắc thông tin tối thiểu_:
thẻ không bao giờ được hỏi về nhiều hơn một điều
(những người am hiểu công nghệ có thể nói rằng thẻ phải là _nguyên tử_).
Việc vi phạm quy tắc này có thể diễn ra dưới hình thức rõ ràng,
như thực sự hỏi hai câu hỏi.
Tuy nhiên, hầu hết chúng thường liên quan đến những câu hỏi cực kỳ chung chung
với nhiều nội dung ở mặt câu trả lời:

> Câu hỏi: Hãy mô tả về ngôn ngữ lập trình Python.
>
> A: Python là ngôn ngữ lập trình đa mô hình, được biên dịch, cấp cao do Guido von Rossum viết và được Python Foundation duy trì. Ngôn ngữ này thường được sử dụng để quản trị hệ thống, phân tích dữ liệu và tạo mẫu nhanh, và liên tục được xếp hạng trong số năm ngôn ngữ phổ biến nhất trong những năm gần đây.

Đây là một lá bài tệ hại!
Không phải là bạn không muốn biết bất cứ điều gì về Python,
hoặc bất kỳ thông tin nào trong đó được giải thích kém,
mà chỉ là có quá nhiều thông tin.
Nếu bạn không muốn ghi nhớ văn bản của câu trả lời một cách máy móc,
bạn sẽ không bao giờ có thể cung cấp chính xác tất cả thông tin trong đó
như một câu trả lời cho lời nhắc mơ hồ đó.
Nếu bạn quên bất kỳ phần nào của câu hỏi,
bạn sẽ phải trượt
(do đó, lá bài sẽ phải quay lại hầu như mỗi ngày
vì bạn không bao giờ có thể học thuộc lòng tất cả)
hoặc nói rằng bạn nhớ rất rõ khi bạn không nhớ.
Chúng ta có thể dễ dàng chia thành một tá câu hỏi, ví dụ:

> H: Ai đã thiết kế ngôn ngữ lập trình Python?
>>
> A: Guido von Rossum.


H: Nhóm nào duy trì ngôn ngữ lập trình Python?
>
> Trả lời: Python Foundation.

> H: Từ năm 2015, Python đã được xếp hạng trong số \[…số\] ngôn ngữ lập trình phổ biến nhất.
>
> Trả lời: 5

Vân vân.

Cũng đáng lưu ý
có khả năng thông tin trong "mô tả" ban đầu
mà chúng ta không muốn biết ngay từ đầu
và không nên lãng phí thời gian cố gắng học.
Chia nhỏ những gì chúng ta đang học thành các câu hỏi
là một cơ hội tuyệt vời để quyết định
những gì chúng ta cần nhớ
để chúng ta có thể tập trung nỗ lực vào thông tin có giá trị nhất.
Mỗi thông tin bạn học đều tiêu tốn thời gian học
mà bạn có thể sử dụng để học thông tin khác.
Hãy lựa chọn một cách khôn ngoan.

## Câu hỏi phải cho phép chỉ một câu trả lời

Để ôn tập hiệu quả,
phải thấy rõ ngay cả câu hỏi đang được hỏi
và câu trả lời duy nhất nào sẽ được tính là câu trả lời đúng;
quá trình suy nghĩ và câu trả lời của bạn phải giống nhau mỗi khi bạn ôn tập,
về ý nghĩa nếu không phải về cách diễn đạt chính xác.
Điều này có vẻ đơn giản,
nhưng hầu hết người mới bắt đầu thường tạo ra những lá bài
vi phạm một hoặc cả hai quy tắc này.
Thậm chí, ngay cả các chuyên gia cũng thỉnh thoảng làm như vậy.
Chúng ta có thể vi phạm quy tắc này theo nhiều cách khác nhau;
hãy cùng xem xét ba cách phổ biến.

### Cho phép trả lời đúng nhưng không liên quan

Đây là một lần xóa câu hỏi điền khuyết từ bộ bài AP US History của tôi (9 năm trước!).
Trong ký hiệu của tôi về việc xóa câu hỏi điền khuyết,
phần trong {dấu ngoặc nhọn} hiển thị dưới dạng `[...]` ở mặt trước của lá bài,
yêu cầu bạn điền vào chỗ trống;
sau đó toàn bộ câu sẽ hiển thị ở mặt sau.

> Các Điều khoản của Liên bang không có thẩm quyền điều chỉnh {thương mại}.

Điều này đúng và là một điểm quan trọng
(việc thiếu quy định về thương mại là một vấn đề quan trọng đã giúp
thúc đẩy việc tạo ra Hiến pháp Hoa Kỳ, sau các Điều khoản).
Tuy nhiên, có vô số
câu trả lời đúng khác mà chúng ta có thể đưa ra!
Các Điều khoản Liên bang cũng không có thẩm quyền điều chỉnh
các nghi lễ tôn giáo,
thuế,
săn gấu,
hành vi của quốc vương Anh,
hoặc giờ mà hàng xóm của bạn có thể chơi trống khi cửa sổ mở.
Rõ ràng, một số câu trả lời này hợp lý hơn những câu trả lời khác,
nhưng thực tế vẫn là tôi có thể
đưa ra một câu trả lời _đúng_
nhưng không phải câu trả lời ở mặt sau của thẻ.

Nếu điều đó xảy ra trong quá trình xem xét, tôi không rõ mình nên làm gì.
Tôi có thể trượt thẻ, điều này có vẻ sai vì tôi đã đưa ra câu trả lời đúng.
Hoặc tôi có thể vượt qua thẻ, điều này có vẻ sai vì không có bằng chứng
cho thấy tôi nhớ thông tin
mà tôi đã cố gắng ghi nhớ bằng cách tạo thẻ này.
Dù bằng cách nào, tôi cũng không thực sự xem xét thông tin
mà tôi đặt ra để học;
Thay vào đó, tôi đang buộc mình phải ghi nhớ, ngoài câu trả lời thực tế,
_thẻ này đang hỏi tôi điều gì_.
Điều đó có nghĩa là tôi đang hỏi về hai điều
và làm cho việc nhớ thẻ trở nên khó khăn hơn nhiều,
mà không có lợi ích gì – trong cuộc sống thực,
biết một trong những thẻ Anki của tôi được cho là hỏi gì
là thông tin vô ích.

Câu trả lời đúng, khi bạn gặp phải tình huống này trong quá trình xem lại
– và bạn sẽ gặp phải –
là dừng xem lại một lúc và viết lại thẻ.
Chúng ta có thể làm điều này theo nhiều cách, nhưng đây là một khả năng:

> Quan hệ kinh tế và thương mại giữa các tiểu bang
> rất khó khăn theo Điều lệ Liên bang
> vì Điều lệ không trao quyền {điều chỉnh thương mại}.

Tất nhiên, tôi vẫn có thể đưa ra những câu trả lời ngớ ngẩn nếu tôi muốn trái ngược
(Tôi khuyên bạn nên trái ngược – điều đó rất vui).
Nhưng, khi đọc câu hỏi một cách thiện chí,
bây giờ tôi có thể khá tự tin
rằng nếu tôi không nhớ ngay câu trả lời mà tôi định trả lời,
thì có nghĩa là tôi đã quên mất.

### Rơi vào bẫy “ví dụ”

Người mới bắt đầu thường viết những câu hỏi như thế này:

> H: Ví dụ về mạch không tổ hợp là gì?
>
> Đ: Trí nhớ.

Đây chỉ là một trường hợp đặc biệt của “cho phép trả lời đúng nhưng không liên quan”,
nhưng tôi đã thấy điều này rất thường xuyên
Tôi muốn đặc biệt lưu ý đến nó.
Chúng ta gặp phải vấn đề tương tự như trước:
tôi không chỉ phải nhớ rằng trí nhớ là mạch không tổ hợp
(thông tin thực tế mà tôi muốn biết),
tôi còn phải nhớ rằng
ví dụ cụ thể về mạch không tổ hợp
thẻ này muốn tôi đưa ra là “trí nhớ”.
Một phiên bản tệ hơn nữa là
“Hãy đưa ra một số ví dụ về mạch không tổ hợp”.
Với phiên bản này, bạn có thể đưa ra các câu trả lời khác nhau mỗi khi nhìn thấy thẻ,
bao gồm cả những câu trả lời không có trên thẻ,
và vẫn có thể trả lời đúng một cách nào đó!

Đây là một ví dụ khác.
Tôi đã thực hiện điều này chỉ vài ngày trước:

> H: OutSystems: Hãy đưa ra ví dụ về thứ gì đó mà bạn có thể sử dụng tham số đầu vào.
>
> Đ: Trong màn hình chỉnh sửa, bạn sẽ cần truyền mục để chỉnh sửa.

May mắn thay, câu hỏi này rất dễ đúc lại thành một dạng hữu ích,
một khi chúng ta nhận ra rằng nó có vấn đề:

> H: OutSystems: Bạn sẽ sử dụng tham số đầu vào trên màn hình chỉnh sửa như thế nào?
>
> Đ: Để truyền mục, bạn cần chỉnh sửa.

Tuy nhiên, từ _example_
không có trong elf nghĩa là bạn đang làm sai điều gì đó;
các ví dụ trên thẻ của bạn thật tuyệt vời khi được sử dụng đúng cách,
như trong câu hỏi sau:

> Hỏi tại sao mèo không thể nếm được vị ngọt còn con người thì có thể là một ví dụ về tâm lý học {chức năng}.

Tương tự như vậy, quay lại câu hỏi về mạch điện, chúng ta có thể viết:

> Bộ nhớ là một ví dụ về mạch điện {không kết hợp}.

Về bản chất, chúng ta đã đảo ngược ví dụ.
Loại câu hỏi này có mục tiêu cụ thể hơn và dễ trả lời hơn
và cũng có xu hướng là kiến ​​thức hữu ích hơn.
Trong thế giới thực, chúng ta hiếm khi được yêu cầu đưa ra ví dụ về một thuật ngữ trong sách giáo khoa,
nhưng chúng ta thường được hưởng lợi từ việc có thể nhận ra
rằng một cái gì đó là ví dụ về ý tưởng đó.
Và rất có thể,
nếu bạn học ý tưởng đủ tốt để dễ dàng trả lời các câu hỏi có dạng này,
bạn sẽ không gặp khó khăn gì khi đưa ra một số ví dụ về ý tưởng đó nếu cần.

**Lưu ý**:
Hiệu quả của hai câu hỏi ngay bên trên
phụ thuộc phần lớn vào mức độ phức tạp của phân loại của riêng bạn về các chủ đề đó.
Xem xét câu hỏi về trí nhớ,
Tôi biết khá ít về mạch điện,
nên tôi không có khả năng bị nhầm lẫn
về đặc tính nào của mạch điện mà người ta hỏi tôi.
Mặt khác, nếu tôi thiết kế đồ điện tử để kiếm sống,
tôi có thể sẽ cần viết lại thẻ đó với một gợi ý
hoặc một số ngữ cảnh bổ sung
để chắc chắn rằng tôi biết câu trả lời mà nó đang tìm kiếm.
Đây là một trong nhiều lý do khiến thẻ do người khác làm
hiếm khi hiệu quả bằng thẻ do chính bạn làm:
bạn là người duy nhất biết tín hiệu nào sẽ mang lại cho bạn kết quả tốt nhất.

### Cho phép nhiều cách diễn giải khác nhau về một câu hỏi

Trong loại câu hỏi tệ này,
người tạo ra không xác định rõ ràng những gì họ đang cố gắng ghi nhớ
và do đó đưa ra một câu hỏi mơ hồ.

> APUSH: Người Mỹ chuyển đến Texas \[khi nơi này nằm dưới sự kiểm soát của Mexico\]
> {không áp dụng các cách thức của khu vực này và vẫn là người Mỹ trong thâm tâm}.

Đây có phải là _điều_duy nhất_ mà tôi muốn nhớ về người Mỹ chuyển đến Texas không?
Thật sao?
Bây giờ, bất kể câu hỏi này tệ đến mức nào, tôi có thể học được câu trả lời
(thực tế, tôi có lịch sử đánh giá gần như hoàn hảo, thẳng 3 trên thẻ này),
nhưng lời nhắc quá mơ hồ đến nỗi điều duy nhất tôi học được
là "nên điền gì vào chỗ trống
khi tôi được hỏi về người Mỹ chuyển đến Texas",
điều này không có nhiều giá trị trong thế giới thực.

> H: Tại sao tốc độ quay của Trái đất chậm lại?
>
> Đ: Giảm tốc thủy triều.

Câu hỏi này tinh tế hơn một chút, nhưng vẫn có vấn đề.
Vấn đề ở đây là mức độ chi tiết mong muốn không rõ ràng.
Có phải nó đang yêu cầu thuật ngữ mô tả hiện tượng này không?
(Thậm chí có thuật ngữ như vậy không? Chúng ta sẽ không biết từ câu hỏi.)
Hay nó muốn giải thích về các lực liên quan đến giảm tốc thủy triều?

Đây là phiên bản tốt hơn:

> H: Hiệu ứng hấp dẫn nào đang khiến tốc độ quay của Trái đất chậm lại theo thời gian?
>
> Đ: Giảm tốc thủy triều.

Nếu chúng ta không biết thủy triều giảm tốc là gì,
chúng ta cũng muốn thêm một thẻ riêng, hoặc thậm chí là nhiều thẻ,
giải thích quá trình đó.
Điều đó đúng ngay cả khi chúng ta không nghĩ
chúng ta đặc biệt muốn biết thủy triều giảm tốc là gì.
Chúng ta không có lựa chọn nào ở đây:
chúng ta _phải_ biết thủy triều giảm tốc là gì
để thẻ này có thông tin có ý nghĩa.
Ngay cả khi chúng ta chỉ cố gắng vượt qua một kỳ thi bao gồm chính xác câu hỏi này,
thẻ sẽ dễ nhớ hơn nhiều, nhiều khi chúng ta biết ý nghĩa của nó.
Đây là [Quy tắc số 1](http://super-memory.com/articles/20rules.htm): _Đừng học nếu bạn không hiểu._

Một điểm quan trọng khác là việc có những thẻ này
có thể không nhắc nhở chúng ta rằng sự quay của Trái đất _đang_ chậm lại
(xem giai thoại của tôi về `cp -i` ở đầu bài đăng).
Có thể chúng ta không quan tâm đến việc nhớ lại thông tin đó,
và chỉ cần nhớ lý do tại sao,
khi chúng ta gặp phải một tham chiếu đến thực tế là nó đang xảy ra.
Nhưng nếu chúng ta muốn nhớ rằng nó đang xảy ra,
chúng ta cũng có thể muốn thêm một thẻ để nhắc nhở chúng ta,
tham chiếu đến bối cảnh
mà chúng ta nghĩ rằng chúng ta muốn nhớ thông tin này.
Ví dụ, có thể chúng ta quan tâm đến việc vòng quay của trái đất đang chậm lại
vì điều đó có nghĩa là [giây nhuận](https://en.wikipedia.org/wiki/Leap_second)
là cần thiết để giữ cho lịch của chúng ta đồng bộ với chu kỳ ngày/đêm:

> Hỏi: Tại sao giây nhuận được thêm định kỳ vào giờ UTC?
>
> Trả lời: Bởi vì vòng quay của trái đất đang chậm lại theo thời gian, khiến UTC trôi ra khỏi sự liên kết với mặt trời.

Trong mọi trường hợp, như mọi khi,
chúng ta phải dành một chút thời gian để cân nhắc những gì chúng ta muốn biết
để đặt câu hỏi đúng
và mã hóa thông tin theo cách hữu ích.

## Câu hỏi không nên yêu cầu bạn liệt kê các thứ

Khi bạn tìm thấy một danh sách các mục trong bài đọc của mình,
bạn thường có xu hướng tạo một thẻ hỏi
các thành viên của danh sách là gì.
Quy tắc số 9-10 của [Hai mươi quy tắc](http://super-memory.com/articles/20rules.htm) gọi những thứ này là _bộ_
(hoặc _liệt kê_, nếu chúng theo thứ tự cụ thể),
và giải thích rằng chúng là một số thẻ khó và gây ức chế nhất,
vì vậy chúng ta muốn tránh chúng khi có thể.

Thông thường, mọi người tạo ra các bộ vì họ không ’t nhận ra các tập hợp là vấn đề
hoặc vì chúng có vẻ như là điều hiển nhiên nhất để học,
thay vì vì tập hợp thực sự là thứ họ muốn biết.
Trên thực tế, việc có thể nêu tên tất cả các ví dụ hoặc các bộ phận của một thứ gì đó hiếm khi hữu ích.
Tuy nhiên, một ảo tưởng khó chịu có thể khiến nó có vẻ như vậy.
Hãy xem xét động cơ đốt trong,
một ví dụ điển hình về một cỗ máy phức tạp theo nhiều cách được xác định bởi nhiều bộ phận của nó.
Một người có thể nêu tên tất cả các bộ phận của ICE
sẽ có vẻ hiểu rõ về nó.
Nhưng đây là một hiệu ứng, chứ không phải là nguyên nhân.
Nếu bạn có thể nêu tên tất cả các bộ phận của ICE nhưng không biết chúng làm gì,
bạn vẫn không hiểu gì về cách thức hoạt động của nó.
Ngược lại, nếu bạn biết tất cả các bộ phận làm gì và chúng liên quan đến nhau như thế nào,
bạn sẽ dễ dàng hình dung được bố cục của động cơ
hoặc thực hiện theo chức năng của các bộ phận
và đặt tên và mô tả từng bộ phận,
bất kể bạn đã ngồi xuống và học cách đọc thuộc lòng chúng theo thứ tự hay chưa.

Tất nhiên, thỉnh thoảng, việc biết một tập hợp các thứ thực sự hữu ích.
Trong trường hợp này, bạn có thể cải thiện hiệu suất của mình đáng kể bằng cách
(a) học và hiểu đầy đủ từng thành viên riêng lẻ của tập hợp
thông qua các thẻ riêng biệt; và
(b) sắp xếp tập hợp thành một phép liệt kê
và phát triển một phương tiện ghi nhớ như từ viết tắt cho thứ tự.
(Tôi muốn tuân thủ chặt chẽ nguyên tắc thông tin tối thiểu
bằng cách tạo hai thẻ cho phần (b),
một thẻ hỏi phương tiện ghi nhớ của tôi là gì
và thẻ còn lại yêu cầu tôi sử dụng phương tiện ghi nhớ để đưa ra câu trả lời.)
[Hai mươi quy tắc](http://super-memory.com/articles/20rules.htm) có một ví dụ hay
về việc sử dụng phương pháp này để học các quốc gia trong EU (quy tắc số 9),
mặc dù nó không bao gồm phương tiện ghi nhớ.
Nhưng trước khi bạn học một tập hợp, ngay cả theo cách hiệu quả,
hãy dành thời gian suy ngẫm xem liệu nó có thực sự hữu ích hay không.

Ghi nhớ các văn bản nguyên văn như thơ hoặc bài phát biểu là một trường hợp đặc biệt của phép liệt kê.
Trong trường hợp này, việc xóa các ô trống trùng nhau sẽ hữu ích,
kiểm tra một dòng trên mỗi thẻ
theo cách khiến bạn cuối cùng đọc thuộc lòng từng dòng trong ngữ cảnh của nó.
Tiện ích bổ sung Anki phổ biến của tôi [LPCG](https://ankiweb.net/shared/info/2084557901) (Trình tạo ô trống lời bài hát/thơ)
có thể giúp bạn tạo thẻ từ những văn bản như vậy.

## Câu hỏi không nên yêu cầu trả lời có hoặc không

Có lẽ kỳ lạ là tôi thấy rằng những câu hỏi có câu trả lời là "có" hoặc "không"
khó nhớ hơn những câu hỏi chứa nhiều thông tin hơn.
Chúng cũng có xu hướng ít hữu ích hơn.
Nếu bạn tạo và học các thẻ hỏi những câu hỏi sâu hơn,
bạn vẫn có thể trả lời "có" hoặc "không" đúng
nhưng cũng biết thêm thông tin về lý do tại sao lại như vậy.

Sau đây là một ví dụ từ bộ bài thiết kế phần cứng máy tính của tôi:

> Hỏi: Phân đoạn có được sử dụng trên bộ xử lý hiện đại không?
>
> Trả lời: Không, nó đã bị xóa trong nền tảng x86-64.

Thật thú vị, bạn có thể thấy rằng thực ra tôi đã đưa thông tin
cần thiết để tạo ra một câu hỏi hay hơn vào câu trả lời.
Tuy nhiên, câu trả lời là một nơi tồi tệ cho loại thông tin này:
bạn không bao giờ được yêu cầu chủ động nhớ lại
và bạn chỉ nhìn vào nó trong một phần nhỏ thời gian bạn nhìn vào câu hỏi,
vì vậy bạn không có khả năng ghi nhớ nó.
Thay vào đó, chúng ta có thể viết lại thẻ:

> Phân đoạn là phổ biến trên các bộ xử lý cũ hơn
> nhưng đã bị xóa bắt đầu từ nền tảng {x86-64}.

Lưu ý rằng khi tìm hiểu sự thật này
(phân đoạn đã bị xóa trong nền tảng bộ xử lý nào?),
chúng ta vẫn biết rằng phân đoạn
không còn được sử dụng trong các bộ xử lý hiện đại nhất,
nhưng chúng ta cũng biết chính xác khi nào nó bị xóa
và chúng ta có thể mong đợi tìm thấy nó trong những loại bộ xử lý nào
(với điều kiện chúng ta biết đôi chút về bộ xử lý, điều mà tôi không mong đợi bạn biết!).

Chúng ta cũng có thể cân nhắc tạo một thẻ,
ngoài hoặc thay cho thẻ ở trên,
hỏi _tại sao_ phân đoạn đã bị xóa trong nền tảng x86-64.
Tất cả phụ thuộc vào chính xác những gì chúng ta muốn biết,
nhưng các câu hỏi _tại sao_ thường là những bổ sung có giá trị.

Mặc dù vậy, tôi vẫn thấy mình thỉnh thoảng viết các câu hỏi có/không,
đặc biệt là khi tôi đang trong giai đoạn đầu tìm hiểu một chủ đề.
Đôi khi bạn vẫn chưa biết _lý do_,
và tốt hơn là bạn chỉ cần biết một điều gì đó là hoặc không,
thay vì phải tìm kiếm và học một loạt các chi tiết
chỉ để có thể cải thiện một thẻ ghi nhớ.
Có lẽ sau này, bạn sẽ có thêm hiểu biết để viết lại thẻ.

Điều đó đưa ra một điểm quan trọng: các câu hỏi không phải là bất di bất dịch.
Bạn thường sẽ bỏ lỡ các vấn đề tiềm ẩn với các câu hỏi mới của mình
cho đến khi bạn bắt đầu xem lại chúng,
và đôi khi bạn sẽ học một thẻ
và nhận ra sau nhiều tuần hoặc nhiều tháng
sau khi đọc một tài nguyên hoàn toàn khác
rằng bạn đã bỏ lỡ một số bối cảnh quan trọng
hoặc hiểu biết ban đầu của bạn hoàn toàn sai.
Bạn nên sử dụng nút chỉnh sửa thoải mái trong khi xem lại
(trong Anki, nhấn `e` để chỉnh sửa thẻ hiện tại và Escape khi bạn hoàn tất).
Nếu bạn phát hiện ra một vấn đề với một thẻ mà bạn không thể sửa ngay
– có thể bạn đang xem lại trên điện thoại
và bạn cần tra cứu một cái gì đó trong một cuốn sách ở nhà để sửa nó –
hãy sử dụng chức năng “đánh dấu”,
sẽ thêm thẻ “đã đánh dấu” vào thẻ của bạn.
Khi bạn có một vài phút rảnh rỗi, và trước khi bạn quên mất vấn đề là gì
– Tôi thích làm điều này một lần một tuần hoặc lâu hơn –
hãy tìm kiếm `tag:marked` trong trình duyệt
và chỉnh sửa các thẻ một cách thích hợp,
sau đó bỏ đánh dấu chúng một lần nữa.

## Câu hỏi phải không có ngữ cảnh

_Không có ngữ cảnh_ ở đây có nghĩa là [ngữ pháp không có ngữ cảnh](https://en.wikipedia.org/wiki/Context-free_grammar),
tức là ngữ pháp trong đó
diễn giải đúng của bất kỳ câu nào
không phụ thuộc vào môi trường xung quanh.
Nói cách khác, câu hỏi của bạn
phải dễ hiểu 100% mà không cần bất kỳ ngữ cảnh xung quanh nào;
nếu bạn tìm thấy một câu hỏi được viết trên một tờ giấy
mà ai đó đánh rơi trên phố,
bạn sẽ có thể hiểu chính xác câu hỏi đang hỏi gì.
Yêu cầu thiết kế này có hai dạng chính.

**(1)**
**Chủ đề hoặc ngữ cảnh phải được nêu ở phần đầu**
**hoặc gần phần đầu câu hỏi,**
để chuẩn bị cho trí nhớ của bạn để lấy đúng loại thông tin
và để tạo điều kiện cho việc xem lại các thẻ từ các chủ đề khác nhau được trộn lẫn,
nhiều người tin rằng điều này sẽ cải thiện khả năng sáng tạo.
Ví dụ, trong một số câu hỏi của tôi ở trên,
bạn đã thấy các từ hạn định ở phần đầu câu hỏi
như `OutSystems:` hoặc `APUSH:`.
Một từ mô tả chủ đề được đưa vào câu cũng có thể hiệu quả,
mặc dù [Quy tắc số 16](http://super-memory.com/articles/20rules.htm) khuyến nghị sử dụng tiền tố
để bạn có thể chắc chắn rằng não của mình bắt đầu đúng cách.

Nếu bạn không làm điều này,
bạn sẽ thường thấy mình hiểu sai câu hỏi –
ngay cả khi câu hỏi rõ ràng trong bối cảnh bạn viết,
khi bạn thấy nó trong bối cảnh bài đánh giá của mình, nó có thể không rõ ràng như vậy.
Trên thực tế, ngay cả khi bạn _không_ trộn lẫn các câu hỏi từ các lĩnh vực khác nhau,
bạn vẫn có thể bị nhầm lẫn.
Ví dụ, tôi đã không còn đếm được số lần
tôi trả lời bằng tiếng Latin
cho một tấm thiệp hỏi về tiếng Đức hoặc tiếng Anh hoặc ngôn ngữ viết tắt của tôi,
ngay cả khi 30 tấm thiệp gần đây nhất của tôi là tiếng Đức!

Bộ sưu tập của tôi chứa đầy hàng nghìn tấm thiệp không có gợi ý ngữ cảnh tốt,
và có lẽ sẽ mất nhiều năm nữa tôi mới nhận ra và sửa tất cả các tấm thiệp có vấn đề.
Hãy tự giúp mình và tham gia thói quen ngay lập tức.
Ngay cả khi bạn chỉ đang học, chẳng hạn, hóa học hữu cơ ngay bây giờ,
hãy đảm bảo rằng các câu hỏi của bạn có thể được hiểu
trong bối cảnh của một khối kiến ​​thức rộng hơn.

**(2)**
**Câu hỏi không nên được xây dựng xung quanh một nguồn cụ thể.**
Bạn có thể _trích dẫn_ các nguồn trên thẻ của mình
(thực ra, việc tham khảo các nguồn
theo cách này hay cách khác là một ý tưởng tuyệt vời,
vì sớm hay muộn bạn cũng sẽ nghi ngờ
về tính xác thực của một số thẻ,
hoặc chỉ muốn tìm thêm thông tin về chủ đề này).
Tuy nhiên, những câu hỏi như thế này cần phải tránh:

> Thống kê: Một trong những trọng tâm chính của phần giới thiệu cuốn sách của chúng tôi
> là việc đo lường {những gì bạn không biết hoặc sự không chắc chắn mà bạn có} là hữu ích.

Trước hết, điều này vi phạm nguyên tắc 1,
vì nó chỉ đề cập đến "cuốn sách của chúng tôi".
Tôi tình cờ biết nó đề cập đến sách giáo khoa nào tại thời điểm này,
nhưng vào một thời điểm khác, tôi có thể không biết!
Nhưng đối với nguyên tắc 2, tôi sẽ không bao giờ nói,
“Này, phần giới thiệu của sách giáo khoa thống kê
mà tôi đã dùng năm thứ ba đại học tập trung vào điều gì?”
Tiền đề của câu hỏi này – mô tả những gì sách giáo khoa nói –
đơn giản là không hữu ích,
và thông tin tôi học được từ tấm thẻ này
sẽ không liên quan trong cuộc sống thực.

Hy vọng rằng, sau khi đọc bài viết này đến tận đây,
bạn đã bắt đầu tiếp thu được tư duy “Tôi muốn biết điều gì?”
và câu hỏi này trông có vẻ tệ với bạn.
Tôi biết với tôi là vậy.

Không phải để lại bài tập cho người đọc, phiên bản này thì sao:

> Thống kê không chỉ là mô tả những gì bạn biết
> mà còn là đặt nó vào bối cảnh {những gì bạn vẫn chưa biết}.

Hãy cẩn thận đừng nhầm lẫn lệnh cấm này với một mô hình rất hữu ích,
cụ thể là hỏi các tác giả cụ thể nghĩ gì về một chủ đề,
hoặc xác định thông tin bằng cách nói rằng người này người kia đã nói điều đó.
Mẫu khác này sử dụng thông tin nguồn hoàn toàn khác:
thay vì đặt câu hỏi _về_ cuốn sách của tác giả,
nó hỏi về ý tưởng _trong_ cuốn sách trong khi giải thích nguồn gốc của nó.
Ví dụ:

> Hỏi: Tại sao, theo Cal Newport, nhiều người thường cùng lúc thực hiện các khám phá?
>
> Trả lời: Những điều này là một phần của “khả năng liền kề” và do đó đặc biệt dễ khám phá.

Đây trở thành một mẫu đặc biệt có giá trị khi bạn
vượt qua kiến ​​thức cơ bản trong sách giáo khoa và các quy tắc hướng dẫn trong một lĩnh vực,
nơi mà sự đồng thuận không còn được coi là điều hiển nhiên nữa.
Bạn không muốn ghi nhớ các ý kiến ​​hoặc lý thuyết mới chớm nở như sự thật!

## Kết luận

Tôi hy vọng những quy tắc này hữu ích với bạn.
Hầu hết những người mới bắt đầu lặp lại theo khoảng cách đều đánh giá thấp rất nhiều
tầm quan trọng của các câu hỏi được diễn đạt cẩn thận,
và tôi vẫn chưa thấy ai viết về các vấn đề phổ biến
ở mức độ chi tiết này.
Các quy tắc được rút ra từ kinh nghiệm của riêng tôi,
nhưng tôi là người đầu tiên thừa nhận rằng tôi không biết mọi thứ về cách viết thẻ;
nếu có bất cứ điều gì, tôi càng dành nhiều thời gian để học,
tôi càng nhận ra mình không hiểu nhiều điều!
Tôi muốn biết liệu những người khác có những trải nghiệm khác không
hoặc đã xác định được các quy tắc bổ sung theo cùng một cách không.

Tất nhiên, các quy tắc được tạo ra để bị phá vỡ,
đặc biệt là khi bạn có nhiều kinh nghiệm hơn,
nhưng nếu bạn bắt đầu bằng cách tìm cách tuân theo những điều này,
bạn sẽ tránh được nhiều cạm bẫy phổ biến
khiến việc lặp lại cách quãng kém hiệu quả hơn so với khả năng hoặc lẽ ra phải có đối với nhiều người.