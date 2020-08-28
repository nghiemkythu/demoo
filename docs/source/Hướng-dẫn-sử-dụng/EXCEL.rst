########################################
XỬ LÝ, BIỂU DIỄN SỐ LIỆU BẰNG EXCEL
########################################

.. figure:: https://imgur.com/a/vFwHvP7
    :width: 200px
    :align: center
    :height: 100px
    :alt: 

.. contents:: 
    :depth: 3
    :local:

1. Tại sao dùng các chương trình bảng tính?
###########################################

* Các chương trình bảng tính như Microsoft Excel hay Google Sheets là những công cụ thân thiện với người mới và hiệu quả trong việc quản lý và biểu diễn dữ liệu, đặc biệt là số liệu, và được dùng rất phổ biến trên toàn thế giới. Ở Việt Nam, các học sinh thường được học Excel trong chương trình Tin học phổ thông và vì vậy, biết cách sử dụng Excel từ cơ bản đến nâng cao.

* Bài viết này giới thiệu những bước thu thập, xử lý và biểu diễn số liệu cơ bản bằng những chương trình bảng tính này.

2. Excel vs Google Sheets
#########################

2.1 Điểm mạnh hơn ở Excel so với Google Sheets
==============================================
* Sở hữu hệ thống tính năng lớn và nâng cao, và nhiều tính năng được nâng cấp hoặc thêm vào ở mỗi phiên bản mới. 

* Là chương trình bảng tính dẫn đầu, và do xuất hiện từ sớm nên có nhiều tài liệu hướng dẫn và có cộng đồng người dùng rộng lớn. Dù vậy, những phiên bản mới hơn của Excel thường đắt và không phù hợp với học sinh.

2.2. Điểm mạnh hơn ở Google Sheets so với Excel
===============================================

* Miễn phí, hỗ trợ tương tác online. 

* Kết nối Google Sheets với các chương trình khác của Google, nên là một công cụ thu thập dữ liệu online hiệu quả. Tuy Excel có thêm tính năng online ở phiên bản mới nhất, nhưng tính năng này đi kèm với giá cao.

Về cơ bản, sự chuyển đổi giữa Excel và Google Sheets chỉ đơn giản là tải lên/ tải xuống các file, vì thế bạn có thể dùng cả hai cùng lúc. Dù vậy, có thể cần phải xác định những tính năng được dùng trong Excel có tồn tại trong Google Sheets (và ngược lại) hay không.


3. Tổng hợp số liệu
###################

3.1 Tổng quát
=============

Sự thu thập, tổng hợp số liệu phụ thuộc vào ứng dụng của bạn. Thông thường, một bảng tính gồm nhiều dòng chứa những entries và nhiều cột để xác định nội dung của từng entry. Nhập hệ thống số liệu này bằng tay thường khá vất vả, vì thế bất kỳ sự tự động hóa nào cũng nên cần được cân nhắc sử dụng trong việc nhập dữ liệu hay sao chép dữ liệu giữa Excel và các hệ thống khác.

3.2 Một số ví dụ trong việc tổng hợp dữ liệu
============================================

Google Forms:

* Là công cụ đơn giản và nhanh gọn để tổ chức khảo sát và thu thập dữ liệu online, và được thiết kế để dùng dễ dàng với Google Sheets. Ở trên là một phiếu khảo sát mình làm để nhận phản hồi từ học sinh của một buổi học online, và những câu trả lời được nhập tự động vào một file bảng tính. 

|pic1|  |pic2| |pic3|

.. |pic1| image:: https://imgur.com/74X62yI.png
   :width: 40%
   :height: 150px

.. |pic2| image:: https://imgur.com/ftGhx3u.png
   :width: 10%

.. |pic3| image:: https://imgur.com/QzWWtWx.png
   :width: 43%


* Ghi lại số liệu thực nghiệm:

 * Những dữ liệu từ thực nghiệm có tầm quan trọng lớn trong việc chứng minh, giải thích những định luật có sẵn cũng như làm bằng chứng cho những định luật mới. Do được thiết kế để quản lý số liệu hiệu quả, những chương trình bảng tính trở nên vô cùng hữu hiệu trong việc ghi nhận những số liệu và sử dụng chúng một cách nhanh chóng.
 * Việc sắp xếp và tính toán thêm những số liệu này sẽ được nói đến ở phần tiếp theo.

|pic1|  |pic2| |pic3|

.. |pic1| image:: https://imgur.com/ftGhx3u.png
   :width: 10%

.. |pic2| image:: https://imgur.com/eRPVxnk.png
   :width: 45%
   :height: 170px


.. |pic3| image:: https://imgur.com/6QQTHNk.png
   :width: 40%

* Dữ liệu từ cảm biến:

 * Khi sử dụng Arduino hay những vi điều khiển khác, để điều khiển những cảm biến, bạn có thể muốn thu thập và biểu diễn số liệu để dễ hiểu hơn. Những phiên bản mới hơn của Excel cho phép truyền trực tiếp dữ liệu từ cổng serial vào file, tuy nhiên đối với những phiên bản cũ hơn, thì bạn có thể cần phải viết chương trình để đọc từ Arduino và nhập vào Excel. 

  Đọc thêm: `Stream Data from Arduino into Excel <https://create.arduino.cc/projecthub/HackingSTEM/stream-data-from-arduino-into-excel-f1bede>`_

.. figure:: https://imgur.com/3t3wUvY.png
    :width: 300px
    :align: center
    :height: 200px
    :alt: Stream Data from Arduino into Excel, Arduino Project Hub

4. Xử lý số liệu
################

* Có một lượng lớn các hàm và các tính năng bạn có thể dùng để điều khiển và tính toán dữ liệu tùy thuộc vào ứng dụng. Bài viết này sẽ không đi sâu vào cách sử dụng những công cụ này, do đã có rất nhiều hướng dẫn online, tuy nhiên theo kinh nghiệm của mình thì những vấn đề bạn gặp phải thường đã được tiếp cận và xử lý bởi những người đi trước, vì thế bạn có thể vừa dùng Excel vừa google cách sử dụng những tính năng mong muốn.

 * Những hàm Excel: đây là những hàm nằm gọn trong từng ô, và được dùng để sắp xếp và tính toán dữ liệu của những ô khác, từ cộng trừ như AVERAGE đến tìm kiếm như LOOKUP. Excel có hệ thống hàm chuyên sâu và hệ thống tài liệu hướng dẫn lớn nhất, dù vậy những hàm thường gặp thường đều được sử dụng trong các chương trình bảng tính.  

  * `Bước đầu làm quen với hàm Excel <https://blog.hocexcel.online/lam-chu-cong-thuc-trong-excel.html>`_
  * `Cách lookup để sắp xếp dữ liệu <https://blog.hocexcel.online/ham-vlookup-trong-excel-huong-dan-su-dung-chi-tiet-va-co-vi-du-cu-the.html>`_

 * Data Analysis: gồm những công cụ để xử lý số liệu, từ trung bình động đến hồi quy các dạng hàm khác nhau. Excel có đi kèm sẵn một số công cụ thường gặp và bạn cũng có thể tải thêm.

  * `Cách sử dụng công cụ data analysis <http://tinhocmos.edu.vn/nhung-dieu-can-biet-ve-cong-cu-data-analysis/>`_
  * `Những add-ins hay <https://infogram.com/blog/6-excel-add-ins-to-find-process-and-analyze-your-data-like-a-pro/>`_

.. figure:: https://imgur.com/WE23cqZ.png
    :width: 300px
    :align: center
    :height: 200px
    :alt: Hồi quy tuyến tính cùng Excel


5. Biểu diễn số liệu
####################

* Đối với những tập hợp dữ liệu nhỏ hơn, ta có thể chỉ cần dùng bảng tính để biểu diễn số liệu. Điều này có thể được làm đơn giản và hiệu quả hơn bằng những **bộ lọc (filters)**, và gần đây hơn là những **bảng pivot**. Những tính năng này giúp dễ dàng thu gọn số liệu và chỉ biểu diễn những gì người dùng muốn xem.

 * `Cách sử dụng bảng pivot <https://www.dantaichinh.com/pivot-table/>`_

* Với những tập hợp dữ liệu lớn hơn, ta có thể dùng những **đồ thị**. Chúng là công cụ hiệu quả để giúp người xem hiểu hơn về số liệu đang được trình bày hoặc tìm ra những tính chất khác mà nhìn bảng tính không thấy được. Có nhiều loại đồ thị khác nhau phù hợp với những ứng dụng khác nhau, và chúng có thể được chỉnh sửa khá dễ dàng. Những đồ thị cũng được cập nhật liên tục.
* Cùng với những bộ lọc và bảng pivot, bạn có thể tạo ra những dashboard mà người dùng có thể tương tác trực tiếp **(interactive dashboard)** và chọn cách biểu diễn số liệu mong muốn. Chúng cũng loại bỏ sự lộn xộn và tạo cho bảng tính của bạn sự đơn giản.

 * `Những bước tạo một dashboard tương tác đơn giản <https://www.educba.com/how-to-create-interactive-excel-dashboard/>`_

.. figure:: https://imgur.com/4PW9CD0.png
    :width: 250px
    :align: center
    :height: 200px
    :alt: GIF source - GIPHY


6. Phụ lục: Thiết kế bằng phần mềm chỉnh sửa vector
###################################################
* Nếu bạn dùng Google Sheets hay Excel từ 2013 trở về trước, bạn có thể nhận thấy design của các đồ thị không quá đẹp cũng như không có nhiều cách để chỉnh sửa giao diện. Nếu bạn dùng được các phần mềm chỉnh sửa vector như Adobe Illustrator hay Inkscape thì có thể tự thiết kế infographic từ các đồ thị của Excel hay Google Sheets.
* Sắp xếp các đồ thị gọn gàng, lưu file dưới dạng PDF.

.. figure:: https://imgur.com/b6ytuoU.png
    :width: 350px
    :align: center
    :height: 220px
    :alt: GIF source - GIPHY

* Khi mở PDF bằng phần mềm chỉnh sửa vector, bạn có thể sửa trực tiếp các đồ thị. Ungroup, xóa những paths không cần thiết và group những paths cần thiết, và thiết kế theo ý của bạn. Voila!

|NYUAD|  |pic2| |pic3|

.. |NYUAD| image:: https://imgur.com/N80grky.png
   :width: 40%
   :height: 150px

.. |pic2| image:: https://imgur.com/ftGhx3u.png
   :width: 10%

.. |pic3| image:: https://imgur.com/uy8g12j.png
   :width: 43%
