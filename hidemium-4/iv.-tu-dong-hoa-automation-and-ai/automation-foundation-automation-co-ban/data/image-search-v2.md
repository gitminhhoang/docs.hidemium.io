# Image Search V2

Để phục vụ cho việc tìm ảnh khi sử dụng automaiton một cách dễ dàng và chính xác hơn, bạn có thể sử dụng node Image Search V2

**Giải thích các trường và lưu ý khi sử dụng node**

![](http://education.hidemium.io/wp-content/uploads/2024/10/Picture1.png)

&#x20;

Giải thích các trường có trong node:

* Button Choose image: Chọn ảnh mà bạn muốn tìm kiếm.
* Switch Take a full screen: Khi để off thì vùng tìm kiếm sẽ lf vùng hiển thị trên màn hình trong 1 trang. Khi để on thì vùng tìm kiếm sẽ là full cả 1 page.
* Find type: Gồm Hide T và Hide K

| Hide T                                                                                                                                                                                                                                                                                                   | Hide K                                                                                                                                                                                                                                                                                                                             |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>–          Hay còn gọi là Tpl (Template Matching)</p><p>–          So sánh trực tiếp một mẫu (template) với một hình ảnh lớn hơn (target image) để tìm vùng tương đồng nhất</p><p>–          Nên sử dụng khi mẫu rõ ràng, không biến dạng, có độ tương phản cao và cần tốc độ xử lý nhanh</p><p> </p> | <p>–          Hay còn gọi là Kaze (Kaze Features)</p><p>–          Phát hiện điểm đặc trưng (feature detection) dựa trên sự biến đổi của gradient (scale-space)</p><p>–          Nên sử dụng khi mẫu có thể bị biến dạng, xoay, chịu nhiễu, cần độ chính xác cao, chấp nhận thời gian xử lý lâu hơn. Cần nhiều CPU hơn</p><p> </p> |

* Enable color finder:

On: Tìm kiếm thao màu sắc thay vì chỉ tìm dựa trên độ sáng

Off: Không dùng màu sắc cho tìm kiếm

* Sensibility: Điều chỉnh độ nhạy của thuật toán tìm ảnh:Giá trị càng cao thì tạo ra các vùng phân biệt rõ ràng hơn, nhưng có thể bỏ qua một số vùng nhỏ hoặc có biên giới không rõ ràng. Giá trị cao hơn sẽ chỉ phát hiện các cạnh rõ ràng, có độ dốc cao, bỏ qua các cạnh mờ nhạt.
* X Coordinates Output Variable và Y Coordinates Output Variable: Khi tìm kiếm ảnh thành công thì tọa độ của ảnh sẽ được lưu lại vào biến mà bạn chọn.

&#x20;

&#x20;

**Lưu ý khi sử dụng node:**

* Khi muốn tìm ảnh ở cuối trang, có một số trang web cần cuộn chuột xuống thì mới load tiếp nên khi ảnh mà bạn muốn tìm nằm ở cuối trang thì trước khi muốn tìm ảnh thì bạn cần phải scroll xuống để load nội dung trang web thì mới có thể tìm được ảnh.
* Tùy vào ảnh và tùy vào từng trang web mà bản phải điều chỉnh node sao cho phù hợp để tìm ảnh thành công.
* Bạn cần điều chỉnh cho đúng để khi chạy campaign ảnh sẽ được tìm thành công và đúng tọa độ của ảnh.
