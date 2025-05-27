# Hướng dẫn Mining

### Mining là gì?
Mình đã viết một [bài viết về Sentence Mining](sentence-mining.md) trong trang. Bạn nên đọc bài viết để tìm hiểu thêm về kĩ thuật học này.

Hiểu một cách cơ bản và theo đúng nghĩa đen, bạn sẽ *đào* kiến thức ngoại ngữ từ nội dung bạn tiêu thụ, đào từ vựng, mẫu câu, cách diễn đạt .v.v... Nhưng thường là *đào* từ vựng.

Thử lấy một câu Tiếng Anh này làm ví dụ:

> Then, the ritual begins: a series of daily tasks, guided by muscle memory and his **immutable** routine.

Trong câu này có từ **immutable** là mình chưa biết chẳng hạn. Sau khi tra từ này trên từ điển xong thì mình biết từ này có nghĩa là **not changing, or unable to be changed**. Bây giờ mình sẽ đưa từ vựng, nghĩa của từ và câu ví dụ vào Anki. Đây được gọi là Mining.

### Anki + Yomitan

Để có thể sử dụng Yomitan với Anki thì bạn cần tải addon AnkiConnect cho Anki, bạn tải Addon trên [trang này](https://ankiweb.net/shared/info/2055492159)

Sau đó, hãy [tải bộ thẻ mẫu bằng cách bấm vào đường dẫn này](img/mining/template-deck.apkg) rồi **Import** và trong Anki.

Giờ chuyển sang Yomitan, sau khi đã cài đặt AnkiConnect như ở trên thì hãy di chuyển đến mục **Anki** trong cài đặt của Yomitan. Cần mở ứng dụng Anki khi bạn sử dụng Yomitan để tạo thẻ. Nếu bạn thành công thì sẽ có dòng **Connection Status: Connected** ở dưới dòng **Enable Anki Integration**.

![alt text](img/mining/enable-anki.png)

Sau đó, hãy mở **Config Anki card format...**.

Về phần **Deck** và **Model** thì bạn hãy chọn **Model** là **English** (Nếu bạn tải bộ thẻ mình để ở trên), còn **Deck** là bộ thẻ mà bạn sẽ lưu các thẻ học của mình lại, bộ thẻ này thì bạn cần tự tạo bằng cách bấm vào **Create Deck** ở màn hình chính của Anki.

Tiếp theo, hãy sao chép những cài đặt sau vào mẫu thẻ (Nếu bạn sử dụng bộ thẻ mẫu mình đã để ở trên):

| Field | Value |
| --- | --- |
| `Word` | `{expression}` |
| `Sentence` | `{cloze-prefix}<b>{cloze-body}</b>{cloze-suffix}` |
| `Meaning` | `{glossary-first-brief}` |
| `Audio` | `{audio}` |

Nó sẽ trông như thế này trong phần cài đặt của Yomitan

![alt text](img/mining/anki-template.png)

Khi bạn tra từ và bấm vào dấu `+` màu xanh lá cây thì nó sẽ tạo thẻ tự động trong Anki và bạn cần bật Anki khi sử dụng Yomitan để tạo thẻ (Nếu bạn chỉ tra từ mà không tạo thẻ thì không cần bật Anki nha).

Đây là một ví dụ mẫu thẻ trên Anki.

![alt text](img/mining/front-anki.png)

![alt text](img/mining/back-anki.png)


### Anki + Goldendict
Mình chưa thực hiện bao giờ nhưng bạn có thể sử dụng Goldendict-ng để thực hiện điều này.

**Đọc thêm**: [Anki Integration](https://xiaoyifang.github.io/goldendict-ng/topic_anki/) từ phần Documentation của ứng dụng để tham khảo cách cài đặt.