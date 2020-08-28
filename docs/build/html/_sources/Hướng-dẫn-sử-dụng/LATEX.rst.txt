.. Imgur album của bài viết: https://imgur.com/a/BcvtIP0

.. figure:: https://i.imgur.com/K94vtnx.jpg
	:width: 100%
	:align: center
	:alt: Ảnh lỗi
	:figclass: align-center

#######################################################
HƯỚNG DẪN SỬ DỤNG LaTeX
#######################################################

.. topic:: Tổng quan bài viết
    
   LaTeX nhìn có thể phức tạp, tuy vậy việc bắt đầu sử dụng LaTeX đơn giản hơn bạn nghĩ. Bài viết này dành cho những người chưa có nền tảng LaTeX, và nhằm mục đích giới thiệu những bước cơ bản để bạn bắt đầu viết được bài viết đầu tiên bằng LaTeX.

	:Writer: Minh Quân

.. contents:: Mục lục
	:depth: 3
	:local:

1. LaTeX là gì?
=======================================================

LaTeX là một hệ thống soạn thảo văn bản được sử dụng phổ biến để
thông tin và xuất bản các tài liệu khoa học trong nhiều lĩnh vực, và
đặc biệt LaTeX *là* hệ thống soạn thảo Toán tiêu chuẩn.

Đối với những phần mềm soạn thảo trực quan như MS Word hay Google
Docs, người viết vừa viết nội dung văn bản vừa sắp xếp vị trí các
hình ảnh, căn lề, in đậm in nghiêng, v.v... (quá trình định dạng)
ngay trên màn hình.

Ngược lại, người sử dụng LaTeX viết nội dung văn bản đơn giản cùng
các lệnh để hướng dẫn bộ phận đọc và thực hiện các lệnh
(**compiler**) thực hiện quá trình định dạng theo hệ thống có sẵn.
Vì vậy, những phần mềm LaTeX khác nhau sẽ cùng xuất ra một văn bản
giống nhau nếu được đưa vào cùng một file văn bản LaTeX. Hệ thống
định dạng này được gọi là TeX, và những file lệnh LaTeX có đuôi
.tex.

2. Tại sao sử dụng LaTeX
=======================================================

Nhờ việc đẩy phần định dạng văn bản cho máy tính, người dùng LaTeX
có thể chỉ cần dùng bàn phím để soạn thảo những văn bản có các thành
phần phức tạp như Toán hay các ngôn ngữ nhiều nét như tiếng Phạn
(Sanskrit) và Hy Lạp (Greek). Nhờ có hệ thống đi kèm có thể định
dạng nhiều dạng văn bản và các phần của chúng, LaTeX là công cụ hữu
ích để nhanh chóng tạo mục lục, trích dẫn nguồn và giúp toàn văn bản
có sự bố trí liền mạch.

Nhờ có cộng đồng dùng LaTeX khổng lồ mà LaTeX ngày càng có nhiều
tính năng, nhất là rất nhiều **packages** - những gói lệnh bạn có
thể cài đặt để thực hiện nhiều chức năng khác nhau - và hàng trăm
templates - những dạng văn bản đã được định dạng sẵn, bạn chỉ cần
tải về và sử dụng. Những templates sẽ được nói thêm trong phần
**5.5.**.

3. Thiết lập & viết đoạn LaTeX đầu tiên
=======================================================

3.1. Soạn thảo online
-------------------------------------------------------

Cách đơn giản nhất để bắt tay vào học LaTeX ngay mà không cần thiết
lập là dùng một trong các trang web chỉnh sửa file LaTeX
(**editors**) online. Các công cụ phổ biến là
`Overleaf <https://www.overleaf.com/>`__,
`Verbosus <https://www.verbosus.com/>`__ hay
`Papeeria <https://papeeria.com/>`__. Overleaf và Papeeria có hỗ
trợ cộng tác để nhiều người có thể chỉnh sửa 1 file (hay 1 project)
cùng lúc, tuy vậy Overleaf vẫn có giới hạn và bạn phải trả phí để có
nhiều cộng tác viên hơn. Verbosus không có tính năng này, tuy vậy có
hỗ trợ chỉnh sửa file trên nền tảng Android và iOS.

Tuy vậy, một điểm trừ của các công cụ soạn thảo online là luôn cần
có kết nối internet mạnh để liên tục tải và hiện file pdf từ server.

3.2. Soạn thảo offline
-------------------------------------------------------

Nếu bạn muốn sử dụng được LaTeX trên máy tính, bạn sẽ cần tải và cài
đặt hệ thống định dạng văn bản TeX (**TeX** **distribution**) và
editor để chỉnh sửa file:

-  Các TeX distributions: đối với Windows, bạn có thể tải và cài đặt `TeX Live <https://www.tug.org/texlive/acquire-netinstall.html>`__ hay `MiKTeX <https://miktex.org/>`__. Đối với Mac OS có `MacTeX <http://tug.org/mactex/>`__, và  \*BSD và GNU/Linux cũng có thể dùng `TeX Live <https://www.tug.org/texlive/acquire-netinstall.html>`__.

-  Các editors phổ biến: `TeXmaker <http://www.xm1math.net/texmaker/>`__, `TeXstudio <http://www.texstudio.org/>`__, `Emacs <https://www.gnu.org/s/emacs/>`__, `TeXworks <http://www.tug.org/texworks/>`__, v.v… Chỉ cần tải về và cài đặt là bạn có thể bắt đầu chỉnh sửa file LaTeX.

Bài viết này sẽ dùng editor TeXstudio trong các hình ảnh, nhưng tất
nhiên bạn có thể thử nghiệm với các editor khác và dùng cái mình
thích nhất.

3.3. Viết đoạn LaTeX đầu tiên
-------------------------------------------------------

Để bắt đầu viết, bước đầu bạn có thể tạo một file .tex trong editor
yêu thích của mình. LaTeX, một cách đơn giản, là văn bản và các lệnh
để định dạng văn bản. Các lệnh bắt đầu bằng ký tự  ``\``, và những
keyword để xác định hoạt động của lệnh (**arguments**) hoặc phần văn
bản bị câu lệnh tác động đến được để trong dấu ngoặc móc ``{}``.

|image0|

Một văn bản cơ bản nhất (không có nội dung) có dạng:

.. code-block:: tex

	\documentclass{article}   
	\begin{document}
 
	\end{document}

Chức năng của từng lệnh:

-  ``\documentclass{article}``: dùng để thiết lập loại văn bản (**class**).
   Có nhiều loại văn bản khác nhau như ``article``, ``report``, ``book``,… với cách
   trình bày nội dung khác nhau mà bạn có thể dùng.

-  ``\begin{document}`` và ``\end{document}``: các câu lệnh ``\begin{}`` và
   ``\end{}`` được dùng để bắt đầu và kết thúc những phần văn bản (các
   **environments**) khác nhau, ở đây là thân văn bản.

Văn bản được viết trực tiếp vào các dòng. LaTeX tự động nối liền các
dòng liền kề, vì vậy bạn cần **cách 2 dòng** giữa các đoạn văn hoặc
đặt ``\\`` cuối đoạn đầu, nhưng đặt như vậy LaTeX sẽ không tự động vào
lề giúp bạn.

.. code-block:: tex

	\documentclass{article}   
	\begin{document}  
	Day la doan 1  

	Day la doan 2 \\
	Day la doan 3
	\end{document}

Tùy vào editor, bấm run/compile (thường có dạng nút play) và view
PDF sẽ xuất ra:  

|image2| |image3| |image1|

Để có thể vào lề hoặc bỏ vào lề, bạn có thể dùng ``\indent`` hoặc
``\noindent``. Để gõ được tiếng Việt, bạn phải chỉnh sửa compiler để
dùng XeLaTeX (cách chỉnh tùy vào editor của bạn), cũng như chỉnh sửa
lệnh một chút:

|image4| |image6| |image5|

|image8| |image7|

.. code-block:: tex

	\documentclass{article}
	\usepackage[vietnamese]{babel}  
	\begin{document}
	Đây là đoạn 1
	Đây là đoạn 2   

	% Đây là 1 comment   
	\end{document}  

|image10| |image9|

Câu lệnh ``\usepackage[vietnamese]{babel}`` được dùng để thêm package
hỗ trợ cho việc hiển thị tiếng Việt, và cũng tương tự bạn có thể
dùng để hiển thị các ngôn ngữ khác. Dấu ngoặc vuông ``[]`` được để trước
dấu ``{}`` và chứa những lựa chọn khác nhau (**options**) cho package, ở
đây là ngôn ngữ (vietnamese, english, arabic,...)

Bạn cũng có thể thấy dòng ``% Đây là 1 comment``. Những dòng bắt đầu
bằng ký tự ``%`` là các ghi chú (**comments**) và không hiển thị ra văn
bản, và được dùng để ghi chú giúp mã LaTeX dễ hiểu hơn.

4. Phần preamble của một văn bản
=======================================================

Tất cả mọi thứ ở trước ``\begin{document}`` là phần **preamble**. Trong
phần **3.3.**, bạn đã thấy phần preamble được dùng để thiết lập loại
văn bản, bố trí văn bản, ngôn ngữ, thêm package và nhiều việc khác
nữa.

Ví dụ về một preamble:

.. code-block:: tex

	\documentclass[12pt, a4paper]{article}  
	\usepackage[vietnamese]{babel}
	% Chọn encoding cho file   
	\usepackage[utf8]{inputenc}   
    
	% Sử dụng những environments dành riêng cho phương trình (equation),   
	% căn lề (align) và chia cột (split)   
	\usepackage{amsmath}  
	% Sử dụng thêm ký tự toán học  
	\usepackage{amssymb}  
	% Sử dụng thêm những thứ khác  
	\usepackage{amsthm, bm}   
    
	% Sử dụng để viết Lý   
	\usepackage{physics}  

Preamble này giúp bạn có thể bắt đầu nhập các bài báo (articles) về
Toán và Lý. Lệnh ``\documentclass[12pt, a4paper]{article}`` xác định
dạng văn bản, những option thêm là kích cỡ font 12pt và cỡ giấy
a4paper. Lệnh ``\usepackage[utf8]{inputenc}`` xác định dạng mã hóa
(encoding) của file và giúp bạn có thể nhập mọi ký tự trong bảng
Unicode. Bạn có thể đọc thêm cách sử dụng package
`amsmath <https://mirror-hk.koddos.net/CTAN/macros/latex/required/amsmath/amsldoc.pdf>`__
và
`physics <http://mirrors.ibiblio.org/CTAN/macros/latex/contrib/physics/physics.pdf>`__,
hoặc dùng Google để tìm các packages khác phù hợp với văn bản của
mình.

Trong phần này, bạn cũng có thể xác định trước tiêu đề, tác giả của
văn bản và ngày viết văn bản:
    
.. code-block:: tex

	\title{Văn bản đầu tiên}
	\author{Nhâm Quân}   
	% \date{25 tháng 7, 2020}    
	% Hoặc dùng \today để LaTeX tự động sử dụng ngày xuất văn bản    
	\date{\today}   

Sau đó, trong phần thân văn bản ta thêm lệnh ``\maketitle`` ở đầu:

.. code-block:: tex

	\begin{document}    
	\maketitle  
	Đây là toán:
	$\biggl[\sum_i a_i\Bigl\lvert\sum_j
    x_{ij}\Bigr\rvert^p\biggr]^{1/p}$    
	\end{document}  

|image11|

5. Định dạng & sắp xếp văn bản đơn giản
=======================================================

5.1. Định dạng chữ
-------------------------------------------------------

Nhờ có hệ thống lệnh và package đa dạng, LaTeX cho phép bạn định
dạng, sắp xếp các chữ và ký tự một cách có tổ chức và linh hoạt. Sau
đây là danh sách một số lệnh định dạng chữ cơ bản thường được sử
dụng:

-  Kích thước chữ: có 10 lệnh để thay đổi kích thước chữ, và sau mỗi
   lệnh kích cỡ chữ giữ nguyên đến lệnh tiếp theo.

.. code-block:: tex

	\tiny Siêu nhỏ \\
	\scriptsize Rất nhỏ \\    
	\footnotesize Nhỏ vừa \\  
	\small Hơi nhỏ \\
	\normalsize Bình thường \\    
	\large Hơi lớn \\
	\Large Lớn vừa \\
	\LARGE Khá lớn \\
	\huge Rất lớn \\  
	\Huge Siêu lớn
    
|image13| |image12|

-  Cách điệu chữ: các lệnh sử dụng cho các hoàn cảnh ngữ pháp, văn bản
   khác nhau, và phần nội dung bị ảnh hưởng bởi lệnh được đặt trong dấu
   ``{}``.

.. code-block:: tex

	\textbf{In đậm} \\  
	\textit{In nghiêng} \\  
	\underline{Gạch chân} \\    
	Chữ\textsuperscript{viết trên} \\   
	Chữ\textsubscript{viết dưới} \\
	\texttt{Đổi font máy đánh chữ} \\   
	\textrm{Đổi font serif (roman)} \\  
	\textsf{Đổi font sans-serif}
    
|image14| |image15|    

Trong nhiều trường hợp, ta có thể sử dụng ``\emph{}`` (emphasis - nhấn
mạnh) thay cho ``\textit{}``, do LaTeX có thể tự động xem xét hai hay
nhiều ``\emph{}`` lồng vào nhau mà định dạng chữ nghiêng hay thẳng.

5.2. Phần (parts), chương (chapters) và mục (sections)
-------------------------------------------------------

Những câu lệnh để phân chia và sắp xếp các phần văn bản là khác nhau
tùy loại văn bản. Xét văn bản sau:

.. code-block:: tex

	\part{Một văn bản LaTeX}  
	\chapter{Mở bài}    
	\section{Phần một}  
	Đây là phần đầu tiên của chương một.
    
	\section{Phần hai}  
	Đây là phần tiếp theo, cũng là phần cuối chương một.
    
	\chapter{Kết bài}   
	Chương hai không được chia phần do nội dung khá ngắn.    

Văn bản trên được chia thành ba bậc. Lệnh ``\section{}`` là đơn giản
nhất, dùng để xác định các mục và có thể được sử dụng ở mọi loại văn
bản. Lệnh ``\part{}`` và ``\chapter{}`` có thể được dùng trong loại ``report``
và ``book``, dùng để phân chia các phần và chương. Mỗi chương sẽ bắt đầu
ở trang mới, còn tên mỗi phần sẽ được đặt ở một trang riêng. Tên của
các bậc chia được đặt trong ``{}``. Đoạn mã trên sẽ xuất ra văn bản
sau: |image16|

Bạn cũng có thể chia các sections thành các phần nhỏ hơn
(subsections), mỗi bậc chia ta thêm một cụm ‘-sub’ vào trước lệnh
``\section{}``. Bậc nhỏ nhất có sẵn là subsubsection, tuy vậy bạn `có
thể định nghĩa
thêm <https://tex.stackexchange.com/questions/60209/how-to-add-an-extra-level-of-sections-with-headings-below-subsubsection>`__
những bậc thấp hơn hoặc dùng ``\paragraph{}`` và
``\subparagraph{}``.

.. code-block:: tex

	\section{Phần một}  
	Đây là phần đầu tiên của chương một.
	\subsection{Câu một}    
	\subsubsection{Ý một}   
	Hãy nêu phương trình năng lượng các bậc của nguyên tử hidro mẫu Bohr.    
	\subsection*{Đáp án câu một}
    
|image18| |image17|

Bạn cũng có thể thấy lệnh ``\subsection*{Đáp án câu một}``. Nếu đặt
dấu sao ``*`` vào trước ngoặc móc, các lệnh chia bậc sẽ không đánh số
phía trước tên.

5.3. Phần tóm tắt (abstract) và mục lục (table of contents)
-----------------------------------------------------------

Khi viết văn bản về quá trình nghiên cứu, có thể bạn sẽ cần viết
phần tóm tắt (abstract) cho bài viết của mình. LaTeX đã kèm sẵn
environment ``abstract``, tự động định dạng phần tóm tắt, mà bạn có thể
đặt ở đầu văn bản của mình.

.. code-block:: tex

	\begin{document}   
	\begin{abstract}   
    	Đây là phần tóm tắt văn bản của bạn.    
	\end{abstract}
	\end{document}
    
|image20|  |image19|

Để thêm mục lục vào văn bản một cách tự động, bạn có thể dùng
``\tableofcontents``.

.. code-block:: tex

	\part{Một văn bản LaTeX}
	\chapter{Mở bài}
	\section{Phần một}   
	\subsection{Câu một}
	\subsubsection{Ý một}    
	\addcontentsline{toc}{subsection}{Đáp án câu một}     
	\subsection*{Đáp án câu một}
    
	\section{Phần hai}
    
	\chapter{Kết bài}
    
|image22| |image21|

Trong phần mã của văn bản trên, bạn có thể thấy lệnh
``\addcontentsline{toc}{subsection}{Đáp án câu một}``. Lệnh này được
dùng để thêm các bậc chia không được đánh số hoặc các phần tử khác
vào mục lục (ở đây là *Đáp án câu một*), có các arguments sau:

-  ``subsection``: bậc mình muốn thêm.

-  ``Đáp án câu một``: tên tương ứng của bậc đó.

5.4. Các file LaTeX mẫu (templates)
-------------------------------------------------------

Những phần trên (hy vọng) đã giúp bạn biết cách sắp xếp văn bản đơn
giản trong LaTeX. Tuy vậy, khả năng của LaTeX rất lớn, và thay vì
mày mò thiết kế từng phần bạn có thể tải những templates - file hay
tập hợp các file LaTeX đã được sắp xếp và định dạng theo các văn bản
có chức năng khác nhau - mà những người khác đã soạn và tải lên
Internet. Những templates cũng được dùng để nhiều tác giả có thể
viết theo phong cách của cùng một nhà xuất bản, hay làm một tiêu
chuẩn bài viết chung cho các nghiên cứu trong cùng một ngành. Việc
đọc và hiểu các templates cũng là một cách hữu hiệu để ta học kho
tàng các lệnh và packages của LaTeX.

Những trang có hệ thống templates lớn là `LaTeX
Templates <https://www.latextemplates.com/>`__,
`Overleaf <https://www.overleaf.com/latex/templates>`__ và `TeX
showcase <https://www.tug.org/texshowcase/>`__.

6. Thêm các danh sách, bảng giá trị, hình ảnh
=======================================================

6.1. Tạo danh sách
-------------------------------------------------------

Có nhiều cách để tạo một danh sách trong LaTeX, nhưng hai cách chính
thường được giới thiệu cho người mới học sử dụng environments
``itemize`` (với danh sách không thứ tự) và ``enumerate`` (với danh sách có
thứ tự).

6.1.1. Danh sách không thứ tự
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Trong environment ``itemize``, mỗi mục phải có lệnh ``\item`` phía trước:

.. code-block:: tex

	\begin{itemize}    
    	\item Mục 1.   
    	\item Mục 2.   
	\end{itemize}	 

|image24| |image23|

Để thay đổi ký tự/chữ đầu mỗi mục, ta để ký tự/chữ đó làm option
trong ``[]``. Ngoài ra, ta cũng có thể lồng nhiều danh sách với nhau,
với số bậc danh sách lớn nhất là 4.

.. code-block:: tex

	\begin{itemize}   
    	\item[+] Mục 1.   
    	\item[\textsuperscript{2}] Mục 2.    
    	\begin{itemize}   
        	\item Mục nhỏ 1.  
    	\end{itemize}
	\end{itemize}
    
|image26|  |image25|

6.1.2. Danh sách có thứ tự
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Environment ``enumerate`` được dùng cho các danh sách cần được đánh số
hoặc chữ theo thứ tự. Mỗi mục cũng cần có lệnh ``\item``, và ta cũng có
thể lồng nhiều danh sách với nhau để LaTeX tự động đánh số/chữ.

.. code-block:: tex

	\begin{enumerate}    
    	\item Mục 1.
    	\item Mục 2.
    	\begin{enumerate}    
        	\item Mục nhỏ 1.
        	\begin{enumerate}    
            	\item Mục nhỏ nhỏ 1.
            	\begin{enumerate}    
                	\item Mục nhỏ nhỏ nhỏ 1.
            	\end{enumerate}  
        	\end{enumerate}  
    	\end{enumerate}  
	\end{enumerate}
    
|image28| |image27|  

6.2. Tạo bảng
-------------------------------------------------------

Sau đây là các lệnh để tạo một bảng đơn giản:

.. code-block:: tex

	\begin{center}  
    	\begin{tabular}{ c c c }    
        	Ô 1 & Ô 2 & Ô 3 \\
        	Ô 4 & Ô 5 & Ô 6  
    	\end{tabular}   
	\end{center}    

Environment ``tabular`` dùng để tạo bảng được đặt trong environment
``center`` để nằm chính giữa văn bản. Sau ``{tabular}`` là các arguments
dùng để xác định tính chất của từng cột, ở đây có 3 chữ c ứng với 3
cột, mỗi cột căn giữa (bạn có thể dùng ``l`` hoặc ``r`` thay thế để căn lề
trái hoặc phải). Các ô trong bảng được ngăn cách bằng các dấu & trên
cùng một dòng, và ta xuống dòng bằng ``\\``. Đoạn LaTeX trên tạo bảng
sau:

|image29|

Ta có thể thêm các đường kẻ khung bằng ký tự ``|`` (dọc) hoặc lệnh
``\hline`` (ngang). Càng nhiều ký tự/lệnh càng nhiều đường.

.. code-block:: tex

	\begin{center}    
    	\begin{tabular}{|r|lc||}    
        	\hline    
        	Cột 1 & Cột 2 & Cột 3 \\
        	\hline    
        	Ô 1 & Ô 2 & Ô 3 \\   
        	\hline    
        	Ô 4 & Ô 5 & Ô 6    
    	\end{tabular}
	\end{center}
    
|image31| |image30|

Nếu muốn, bạn có thể sử dụng argument ``p`` (par-box) thay cho ``rlc`` để
xác định độ rộng của cột bảng:  

.. code-block:: tex

	\begin{tabular}{p{3cm}| p{0.2\textwidth}}    

|image33| |image32|

Ở đây ta sử dụng độ rộng cột làm argument cho ``p`` (3cm và 0.2 (⅕) của
``\textwidth``, với ``\textwidth`` là độ rộng trang văn bản). Nếu muốn vừa
xác định độ rộng vừa căn lề cho cột, bạn sẽ phải sử dụng khá nhiều
lệnh `phức
tạp <https://texblog.org/2019/06/03/control-the-width-of-table-columns-tabular-in-latex/>`__,
nên nếu muốn bạn có thể dùng `công cụ tạo bảng tự
động <https://www.tablesgenerator.com/>`__ trong LaTeX.

6.3. Thêm hình ảnh
-------------------------------------------------------

Để sử dụng được hình ảnh trong văn bản, ta cần sử dụng thêm package

.. code-block:: tex

	\usepackage{graphicx}    

do LaTeX không có sẵn chức năng sử dụng hình ảnh. Package ``graphicx``
cho ta thêm các lệnh ``\includegraphics{đường-dẫn-đến-ảnh/tên-ảnh}`` và
``\graphicspath{{đường-dẫn-đến-ảnh-mặc-định}}``. LaTeX có khả năng truy
cập và quản lý các file và thư mục (**folders**) nằm trong cùng thư
mục với file .tex đang sử dụng, vì vậy đường dẫn đến ảnh trong
``\includegraphics{}`` có thể chỉ cần là tên ảnh - nếu ảnh nằm trong
cùng thư mục chứa file .tex (không cần đuôi tên xác định loại ảnh) -
hoặc là tên thư mục chứa ảnh/tên ảnh với thư mục đó nằm trong cùng
thư mục chứa file .tex. Chú ý rằng, thường LaTeX không hiểu các
đường dẫn có dấu tiếng Việt và dấu cách, vì vậy khi đặt tên file và
thư mục bạn nên bỏ qua chúng hoặc dùng tiếng Anh.

Nếu tất cả ảnh của bạn cùng nằm trong một thư mục, bạn có thể điền
tên thư mục vào ``\graphicspath{}`` để LaTeX lấy đó làm thư mục mặc
định và tìm ảnh bên trong. Lưu ý rằng, đường dẫn trong
``\graphicspath{}`` được bao bởi **2** dấu ngoặc móc, và ta cũng có thể
để nhiều đường dẫn kế bên nhau để LaTeX tìm cùng lúc nhiều thư mục.
Ta cũng có thể xác định chiều ngang của ảnh bằng option ``width`` cho
lệnh ``\includegraphics{}``, và cũng lưu ý cần sử dụng option
``keepaspectratio`` để ảnh không bị méo. Sau đây là các lệnh để thêm ảnh
DaiNganHa nằm trong thư mục HinhAnh > ThienNhien, cũng như xác định
độ rộng ảnh là ``0.9\textwidth`` và ảnh nằm giữa bằng environment
``center``.

.. code-block:: tex

	\usepackage{graphicx}  
	\graphicspath{{HinhAnh/}}  
    
	\begin{document}   
	\begin{center}
    	\includegraphics[width = 0.9\textwidth, keepaspectratio]{ThienNhien/DaiNganHa}    
	\end{center}   
	\end{document}
    
|image34| |image35|   

6.3.1. Sử dụng figures, thêm tựa ảnh (caption), tên (label) và nhắc đến hình ảnh (reference)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Figures là các hình ảnh, các bảng, các đồ thị, giản đồ, v.v… được
đặt vào bài viết để giúp người đọc dễ hình dung và hiểu những ý cần
truyền đạt. Các figures được sử dụng phổ biến trong LaTeX bằng
environment ``figure``, và trong environment bạn có thể gắn tựa ảnh vào
ảnh, đánh số tự động và gộp nhiều ảnh với nhau. Dù khi mới học về
figure bạn có thể gặp phải khó khăn trong việc tìm kiếm các lệnh,
tìm cách đặt vị trí, căn lề,... thì việc nắm bắt cách sử dụng chúng
sẽ giúp bạn hiểu hơn về cách LaTeX hoạt động cũng như tạo những văn
bản đẹp.

Ví dụ về một figure chứa ảnh dải Ngân Hà nói trên:

.. code-block:: tex

	Sau đây, các bạn sẽ được thấy Dải Ngân Hà.  
	\begin{figure}[h!]
    	\begin{center}
        	\includegraphics[width = 0.8\textwidth, keepaspectratio]{ThienNhien/DaiNganHa}    
        	\caption{Thiên hà của chúng ta}    
        	\label{fig:DNH}    
    	\end{center}   
	\end{figure}   
    
	Như bạn thấy ở trong hình \ref{fig:DNH}, Dải Ngân Hà rất đẹp.  

|image37| |image36|

Một số lệnh mới đã được dùng:

-  ``\caption{Thiên hà của chúng ta}``: dùng để thêm tựa đề cho figure.

-  ``\label{fig:DNH}`` và ``\ref{fig:DNH}``: lệnh ``\label{}`` đặt cho figure một
   tên ngắn gọn, và ta có thể dùng tên này để nhắc đến figure trong
   văn bản với lệnh ``\ref{}``. Thông thường, cách đặt tên ngắn gọn là
   ``loại-của-cái-được-đặt-tên:tên-của-nó``, ở đây là loại ``fig`` và tên
   ``DNH``.

Lệnh ``\begin{figure}`` cũng được thêm option ``[h!]`` (chú ý đặt ``[h!]`` sau ``{}``),
dùng để xác định vị trí LaTeX sẽ đặt figure. Văn bản trên khá đơn
giản nên figure được đặt ở vị trí ứng với vị trí lệnh ``\begin{figure}``,
tuy nhiên trong những văn bản dài hơn những figures có thể sẽ nhảy
loạn xạ do LaTeX tự động tìm vị trí vừa vặn để đặt chúng. Vì vậy, ta
có thể thử nghiệm với các ký tự khác nhau:

  **Ký tự** 	**Ý nghĩa**
  ``h`` 	Đặt figure một cách gần đúng tại *đây (here)*, nhưng không phải lúc nào LaTeX cũng đặt ở nơi ứng với vị trí lệnh.   
  ``t`` 	Đặt figure ở *đầu (top)* trang  
  ``b`` 	Đặt figure ở *cuối (bottom)* trang
  ``p`` 	Đặt figure ở *một trang (page)* riêng   
  ``!`` 	Bỏ qua những ràng buộc hệ thống mà LaTeX dùng để xác định vị trí nào là vừa vặn, giúp đặt ảnh đúng chỗ hơn nhưng có thể mất thẩm mỹ.    

Hoặc ta có thể dùng kết hợp nhiều ký tự một lúc: ``[htbp!]``. Ta cũng có
thể dùng ký tự ``H`` gần như tương ứng với ``h!``, giúp figure đặt được đúng
chỗ nhất nhưng phải dùng thêm ``\usepackage{float}``.

7. Viết toán trong LaTeX
=======================================================

Lý do lớn nhất chúng ta dùng LaTeX là vì khả năng viết các công thức
Toán của LaTeX vượt trội hơn hẳn các công cụ soạn thảo khác. Một
package rất hữu dụng để viết Toán là ``amsmath``:

.. code-block:: tex

	\usepackage{amsmath}    

Khi muốn viết Toán, ta phải chuyển sang các environments dành riêng
cho Toán theo hai cách viết: liền mạch với văn bản (**inline**) hoặc
tạo đoạn riêng (**display**).

Ví dụ cho cách viết ``inline``:

.. code-block:: tex

	Định lý Py-ta-go cũng có thể viết dưới dạng phương trình: $a^2 + b^2 = c^2$, với a, b là độ dài các cạnh góc vuông và c là độ dài cạnh huyền của một tam giác vuông.    

|image38|

Bên cạnh ``$...$``, ta cũng có thể dùng ``\(...\)``,
``\begin{math}...\end{math}`` để xác định cách viết inline.

Cách viết ``display`` có hai loại, có đánh số (được xác định bởi
``\begin{equation}...\end{equation})`` và không đánh số (được xác định
bởi ``\[...\]``, ``\begin{displaymath}...\end{displaymath}``,
``\begin{equation*}...\end{equation*})``. Ta có thể dùng thêm các
environments ``align``, ``split`` hay ``multiline`` để sắp xếp các biểu thức, và
bạn cũng có thể dùng hệ thống ``\label{}`` và ``\ref{}`` như trên để nhắc
đến các biểu thức Toán trong văn bản.

.. code-block:: tex

	Năng lượng ứng với bậc n của electron trong nguyên tử hidro mẫu Bohr:   
	\begin{equation}   
    	E_n = -\frac{Z^2 m e^4}{8n^2 h^2 \varepsilon_0^4}   
    	\label{EQ:en}  
	\end{equation}
    
	Thực nghiệm giúp ta tìm được giá trị của các đại lượng trong biểu thức \ref{EQ:en}:    
	\[E_n = -\frac{13,6}{n^2}eV\]   

|image39|

Hệ thống các lệnh và packages của LaTeX là rất lớn, vì vậy bài viết
này sẽ chỉ nêu ra những ý cơ bản có thể giúp ích bạn khi viết Toán
trong LaTeX:

-  Các thừa số trong phép nhân có thể viết liền hoặc ngăn cách bởi các
   dấu cách để tránh việc các phần tử gần nhau bị gộp chung. Nếu muốn
   thêm dấu nhân chấm ‘·’ ta dùng ``\cdot``, để thêm dấu nhân chéo ‘×’ ta
   dùng ``\times``.

-  Biểu thức trên mũ và dưới chân được xác định bằng ``^`` và ``_``. Nếu có
   nhiều phần tử ta có thể bao chúng lại bằng ngoặc móc ``{}``. Ví dụ:
   ``T^{i_1 i_2 \dots i_p}_{j_1 j_2 \dots j_q}`` sẽ tạo |image40|.

-  Phân số được viết bằng ``\frac{tử số}{mẫu số}``.

-  Dấu ∀ (với mọi) và ∃ (tồn tại) được viết bằng ``\forall`` và ``\exists``. ∈
   (thuộc) và ∉ (không thuộc) được viết là ``\in`` và ``\notin``.

-  ≠, ≥ và ≤ được viết là ``\neq``, ``\geq`` và ``\leq``. Dấu suy ra ⇒ và tương
   đương ⇔ được viết là ``\Rightarrow`` và ``\Leftrightarrow``.

-  ℤ, ℝ,... được viết là ``\Z``, ``\R``,...

-  Để viết dấu ngoặc có thể mở rộng để vừa các phần tử bên trong, bạn có
   thể dùng ``\left`` và ``\right`` đi kèm với dấu ngoặc đó. Ví dụ:
   ``\left(...\right)``, ``\left[...\right]``.

-  Phép tổng và tích của dãy số được viết bằng ``\sum`` và ``\prod``, và giới
   hạn trên và dưới được viết bằng ``^`` và ``_`` như trên. Phép tích phân cũng
   được viết giống như thế với lệnh ``\int``.

.. code-block:: tex

	\int_0^1 x^{-x} dx = \sum_{n=1}^{\infty} n^{-n}    

|image41|

-  Hàm không liên tục có thể được viết bằng environment ``cases``:

.. code-block:: tex

	f(x) =    
	\begin{cases}    
    	1 & x=0 \\  
    	2x & x<0 \\
    	x^2 & x>0
	\end{cases}  

|image42|

-  Nếu muốn thêm chữ khi viết Toán, ta dùng lệnh ``\text{}``. Lưu ý rằng do
   LaTeX tự động điều chỉnh các dấu cách trong environments Toán nên ta
   thường cần thêm dấu cách ở đầu hay cuối nội dung chữ: ``AB = 2cm
   \text{ (đpcm)}`` tạo . |image43|

-  Ta có thể tạo bảng trong khi viết toán bằng environment ``array`` thay
   thế cho ``tabular``.

Bạn cũng có thể xem thêm các lệnh xác định các ký tự thường gặp
trong Toán tại
`đây <https://www.caam.rice.edu/~heinken/latex/symbols.pdf>`__.

8. Đọc thêm, các nguồn sử dụng cho bài viết
=======================================================

Sau bài viết, hi vọng bạn đã có những kiến thức nền đủ để bắt đầu sử
dụng LaTeX. Nếu muốn tìm kiếm cách sử dụng một chức năng nào đó, bạn
sẽ thấy Google và các trang hướng dẫn LaTeX như
`Overleaf <https://www.overleaf.com/learn>`__ và
`StackExchange <https://tex.stackexchange.com/>`__ khá hữu dụng.
Dù hầu hết những hướng dẫn về LaTeX trên Internet đều bằng tiếng Anh
các hướng dẫn tiếng Việt cũng đang dần dần xuất hiện. Bạn cũng có
thể dùng các `LaTeX cheat
sheet <https://wch.github.io/latexsheet/latexsheet.pdf>`__ để tìm
những hướng dẫn một cách nhanh chóng.

Bài viết này sử dụng một phần ý tưởng, nội dung từ các nguồn:

-  `Learn LaTeX in 30 minutes,
   overleaf.com <https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Paragraphs_and_newlines>`__

-  `A Beginner Guide to LaTeX,
   princeton.edu <https://www.cs.princeton.edu/courses/archive/spr10/cos433/Latex/latex-guide.pdf>`__

-  `LaTeX Installation,
   wikibooks.org <https://en.wikibooks.org/wiki/LaTeX/Installation>`__

-  `LaTeX Text Formatting,
   latex-tutorial.com <https://www.latex-tutorial.com/symbols/text-formatting/>`__

Các hình ảnh tiêu đề và dải Ngân Hà được lấy từ trang
`Pexels <https://www.pexels.com/>`__.

.. |image0| image:: https://i.imgur.com/UQyaVrI.png
   :width: 1.56250in
   :height: 1.26042in
   :align: middle
.. |image1| image:: https://i.imgur.com/jtkHMB6.png
   :width: 3.07708in
   :height: 1.39554in
   :align: middle
.. |image2| image:: https://i.imgur.com/ZoaYQWP.png
   :width: 2.14583in
   :height: 1.14583in
   :align: middle
.. |image3| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image4| image:: https://i.imgur.com/4950nkI.png
   :width: 3.46354in
   :height: 1.51396in
   :align: middle
.. |image5| image:: https://i.imgur.com/gdxengV.png
   :width: 2.14583in
   :height: 1.75655in
   :align: middle
.. |image6| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image7| image:: https://i.imgur.com/0m6ZHdn.png
   :width: 3.87584in
   :height: 2.03646in
   :align: middle
.. |image8| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image9| image:: https://i.imgur.com/vc9yjG3.png
   :width: 2.68750in
   :height: 1.62500in
   :align: middle
.. |image10| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image11| image:: https://i.imgur.com/xeW0ryl.png
   :width: 5.43958in
   :height: 2.92901in
   :align: middle
.. |image12| image:: https://i.imgur.com/Uy2tiw7.png
   :width: 1.05022in
   :height: 2.31250in
   :align: middle
.. |image13| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image14| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image15| image:: https://i.imgur.com/M1F4QiI.png
   :width: 2.24847in
   :height: 1.86458in
   :align: middle
.. |image16| image:: https://i.imgur.com/a9MA1Dz.png
   :width: 6.04167in
   :height: 1.77184in
   :align: middle
.. |image17| image:: https://i.imgur.com/kgual2V.png
   :width: 4.11667in
   :height: 1.95302in
   :align: middle
.. |image18| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image19| image:: https://i.imgur.com/6Fpeoiw.png
   :width: 2.65625in
   :height: 1.44979in
   :align: middle
.. |image20| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image21| image:: https://i.imgur.com/DdQuiTI.png
   :width: 3.58750in
   :height: 1.91181in
   :align: middle
.. |image22| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image23| image:: https://i.imgur.com/S0acM0X.png
   :width: 1.06031in
   :height: 0.78542in
   :align: middle
.. |image24| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image25| image:: https://i.imgur.com/izDpID3.png
   :width: 2.30625in
   :height: 1.70625in
   :align: middle
.. |image26| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image27| image:: https://i.imgur.com/Cl1Jjtj.png
   :width: 3.31858in
   :height: 1.70833in
   :align: middle
.. |image28| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image29| image:: https://i.imgur.com/seIi68Y.png
   :width: 1.64792in
   :height: 0.87639in
   :align: middle
.. |image30| image:: https://i.imgur.com/PCuL8qx.png
   :width: 3.05625in
   :height: 1.33314in
   :align: middle
.. |image31| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image32| image:: https://i.imgur.com/2wy15AK.png
   :width: 3.18125in
   :height: 0.70864in
   :align: middle
.. |image33| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image34| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image35| image:: https://i.imgur.com/Hx1mi28.png
   :width: 2.77292in
   :height: 1.67292in
   :align: middle
.. |image36| image:: https://i.imgur.com/NDVJgmG.png
   :width: 3.53958in
   :height: 2.99120in
   :align: middle
.. |image37| image:: https://i.imgur.com/jFwWkuI.png
   :width: 0.66095in
   :height: 0.50521in
   :align: middle
.. |image38| image:: https://i.imgur.com/gl7JBvB.png
   :width: 4.33958in
   :height: 0.63286in
   :align: middle
.. |image39| image:: https://i.imgur.com/8AY5gKl.png
   :width: 4.54792in
   :height: 1.48953in
   :align: middle
.. |image40| image:: https://i.imgur.com/OjG7VxH.png
   :width: 0.50208in
   :height: 0.22208in
   :align: middle
.. |image41| image:: https://i.imgur.com/XlxvAiH.png
   :width: 3.58958in
   :height: 1.13936in
   :align: middle
.. |image42| image:: https://i.imgur.com/7NchcjQ.png
   :width: 2.03958in
   :height: 1.09824in
   :align: middle
.. |image43| image:: https://i.imgur.com/hp0l5vv.png
   :width: 1.33333in
   :height: 0.21749in
   :align: middle
