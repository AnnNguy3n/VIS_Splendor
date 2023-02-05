# State
    * [0:6]: Nguyên liệu trên bàn chơi, theo thứ tự Red Blue Green Black White.
    * [6+6*i:12+6*i], i = 0,1,2,3,4: Thông tin của 5 thẻ noble ở trên bàn gồm điểm và giá để mua thẻ. Vị trí nào trên bàn mà không có thẻ thì trong state, tại vị trí tương ứng sẽ chỉ toàn số 0.
    * [36+11*i:47+11*i], i = 0,1,2,...,14: Thông tin của 15 thẻ có thể mua, 12 thẻ đầu tiên là thẻ trên bàn chơi, 3 thẻ tiếp theo là thẻ úp (nếu có). Bao gồm: Điểm của thẻ, loại nguyên liệu được nhận và giá để mua thẻ.
    * [201+12*i:213+12*i], i = 0,1,2,3: Thông tin của 4 người chơi bắt đầu từ bản thân, gồm nguyên liệu, nguyên liệu vv và điểm.
    * [249+3*i:252+3*i], i = 0,1,2: Số lượng thẻ úp các cấp của 3 người chơi đối thủ.
    * [258:263]: Nguyên liệu đã lấy (dùng trong phase lấy nguyên liệu).
    * [263]: Game đã kết thúc hay chưa (1 là kết thúc rồi).
    * [264]: Còn thẻ ẩn cấp 1 hay không
    * [265]: Còn thẻ ẩn cấp 2 hay không
    * [266]: Còn thẻ ẩn cấp 3 hay không

# Action
    * [0:5]: Các action lấy nguyên liệu theo loại.
    * [5:20]: Các action mua thẻ lần lượt tại các vị trí trên bàn chơi và trong tay úp.
    * [20:35]: Các action úp thẻ lần lượt tại các vị trí hiện trên bàn và chồng thẻ ẩn.
    * [35:40]: Các action trả nguyên liệu.
    # [40]: Action bỏ lượt (trường hợp hiếm, khi mà bot không thể thực hiện bất cứ action hợp lệ nào).