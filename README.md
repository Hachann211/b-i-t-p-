<!DOCTYPE html>
<html lang="vi">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tính Diện Tích Hình Chữ Nhật</title>
</head>

<body>
    <h1>Tính Diện Tích Hình Chữ Nhật</h1>
    <label for="length">Chiều dài:</label>
    <input type="text" id="length" placeholder="Nhập chiều dài">
    <br>
    <label for="width">Chiều rộng:</label>
    <input type="text" id="width" placeholder="Nhập chiều rộng">
    <br>
    <button onclick="calculateArea()">Tính Diện Tích</button>
    <p id="result"></p>

    <script>
        function calculateArea() {
            const lengthInput = document.getElementById('length').value;
            const widthInput = document.getElementById('width').value;
            const length = parseFloat(lengthInput);
            const width = parseFloat(widthInput);

            // Kiểm tra nhập liệu
            if (isNaN(length) || isNaN(width)) {
                document.getElementById('result').innerText = "Vui lòng nhập vào số hợp lệ.";
                return;
            }

            if (length <= 0 || width <= 0) {
                document.getElementById('result').innerText = "Chiều dài và chiều rộng phải là số dương.";
                return;
            }

            const area = length * width;
            document.getElementById('result').innerText = `Diện tích hình chữ nhật là: ${area}`;
        }
    </script>
</body>

</html>
