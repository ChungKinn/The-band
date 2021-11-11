# Font

font-family: 'Poppins', sans-serif;/_ áp kiểu font từ gg front_/
font-size: 1.6rem; /_kích thước của font_/
font-weight: 100px; /_độ đậm nhạt của font_/
font-style: italic;/_kiểu chữ in nghiêng_/
}

## .font{

/_ line-height: 1.5; /_ khoảng cách giữa các dòng */
/*text-align: left;/_căn trái(mặc định)_/
/* text-align: right;/*căn phải*/
/*text-align: center;/_căn giữa _/

## letter-spacing: 2px;/_Khoảng cách giữa các kí tự_/

    word-spacing: 5px;/*Khoảng cách giữa cá từ*/
    /*hien thi dau 3 cham tren mot hang*/
    /* white-space: nowrap; */(1hang)
    /* overflow: hidden;(ẩn text)
    text-overflow: ellipsis; */(Hiển thị dấu 3 chấm )
    /*hien thi dau ba cham tu hang thu 3*/
    /* display: -webkit-box;
    -webkit-box-orient: vertical;(Chiều dọc)
    -webkit-line-clamp: 1;/*sau sô dòng hiển thi dau 3 cham*/
    /*overflow: hidden;
    text-overflow: ellipsis;*/
    /*word-break: break-all;/*hien thi rot xuong dong*/
    /*word-break: break-word;/*hien thi rot xuong dong co y nghia*/

}

## ảnh

cover: phủ toàn khối, ản không bị méo
text-decoration: none;(không gạch chân)(href)

## Gradient Trong css:

Background-image: linear-gradient(to right bottom, #fff, ##ffa400);

-Trong đó:  
 +, direction(Hướng): to right(từ trái qua phải), to left(từ phải qua trái), to bottom(từ trên xuống dưới), to top(từ dưới lên trên)
to right bottom(tư trái qua phải rồi chạy xuống dưới).....
120deg
+, color1
color2

## thể áp dụng với chữ gradient:

=) chuyển display: inline-block;
color: transparent;
-webkit-background-clip: text;
background-clip: text;

## Xử lí background overplay gradient (lớp nền phủ nên)

Cái nào nằm trên sẽ viết trước
Vd:
Background-image: linear-gradient(to right bottom, rbga(), rgba()), url();

## Caniuse.com và support(Trình duyệt hỗ trợ)

@support (-webkit-background-clip: text)(Nếu hỗ trợ){
.title{
color: transparent;
linear-gradient(to right bottom, #fff, ##ffa400);
-webkit-background-clip: text;
background-clip: text;

## Sự khác nhau giữa opacity, visibility và display none:

opacity: 0 (vẫn chiếm diện tích có thể nhấn vào được.) (_)Thường được sử dụng với nhau để làm tiêu đề trantion(nhấn vào hiện ra)
visibiti: hidden(vẫn chiếm diện tích những không nhấn vào được) (_)
display: none(không chiếm diện tích và cũng không nhấn vô được)
}

## shadow Trong css:

.shadow{
w20px;
h20px;
background-color: 0px;
margin: 5rem auto;
box-shadow: 5px 5px 10px 5px rbga(255,0,0,0.2);(Dùng F12 để sửa hình ô vuông (Open shadow editer))(outset hiển thị bên ngoài) + inset(hiển thị bên trong)
box-shadow: inset 5px 5px 10px 5px rbga(255,0,0,0.2);
/_box-shadow: x y blur(độ mờ) scale( hiển thị ra ngoài) color(màu)_/
}

## Với chữ shadow:

font-size: 2rem;
font-weiht: bold;
text-shadow: 5px 5px 10px red;(không có scale)

## Độ ưu tiên trong css

Tags < class < id

## Child selector trong CSS:

li:first-child(chọn phần tử đầu tiên)
li:last-child(chọn phần tử cuối cùng)
li:nth-child(_)(chọn phần tử thứ _)
li:nth-last-child(_)(Chạy ngược so với nth-child từ dưới lê trên)
li:not-child((tag class id) :first-child)(chọn tất cả trừ phần tử đầu tiên)
li:nth-child(odd)(chọn phần tử số lẻ)
li:nth-child(even)(chọn phần tử số chẵn)
child-of-type:
li:first-of-type(cái đầu tiên của thẻ li)
li:last-of-type(cái cuối cùng của thẻ li)
li:nth-of-type(_)(chọn phần tử thứ _ của thẻ li)
li:nth-last-of-type(_)(chọn phần tử từ dưới lên \* của the li)

# Muốn chọn thẻ đầu tiên trong thẻ li(con của thẻ li)

VD: <div>

<li>
<span>abc</span>
</li>
</div>

<div>
	<li>
		<span>abc</span>
	</li>
    </div>

# code: li:first-child span{}(chọn thẻ span đầu tiên)

## Combinators CSS:

Cùng cấp với nhau nhưng không nhất thiết phải liền kề: h1 ~ .title{}

## Thuộc tính tranform:

transform: scale scaleX(Chiều ngang) scaleY(Chiều dọc)(kéo theo đường thẳng)
transfrom: rotate(45deg) (Xoay 45 độ)
transform: translateX(10px)(cách chiều ngang 10px) translateY(cách chiều dọc 10px)
Muốn cách bằng với chiều rộng chính nó :
transform: translateX(100%) translateY(100%)
Muốn ra giữa (theo tọa độ xy):
transform: translateX(-50%) translateY(-50%)
Thuộc tính postition absolute:
Ra giữa: left: 50%; top 50%;
Kết hợp vơi tranfrom:
left:50%;top50%
transfrom: translate:(-50%,-50%)
Muốn center theo chiều ngang :
left: 50%
transfrom: translateX(-50%)
Muốn center theo chiều dọc:
top:50%
transfrom: translateY(-50%)
Overlay all(phủ hết):
top: 0;
left: 0;
width:100%
height:100%

top:0;
left:0;
bottom:0;
right:0;
width:auto;
height:auto;

# Overlay theo chiều ngang: Width: 100%;
 top:0; 
 left:0;
 Hoặc có thể thay (width=auto; và thêm right=0;)
# Overlay theo chiều dọc:
height: 100%
top:0;

# đi kèm với thuộc tính poistion còn có z-index:
z-index: 1;
#   T h e b a n d  
 