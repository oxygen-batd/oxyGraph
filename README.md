# Graph
## Khái niệm:
 - Là một đồ thị biểu diễn một tập hợp các đỉnh (V viết tắt của Vertex) và tập các cạnh (E viết tắt của Edges) . Ví dụ dưới: V = { A, B, C, D, F }, E = {AB, AC, BD, DC, CF }
 - Ứng dụng của Grap: Bản đồ, mạng xã hội, ...
 - Neighbors là tập những vertex có connected. Ví dụ: neighbors (A) = { B, C }
 - degree là số lượng vertex có chung connected. Ví du: degree (A) = 2, degree (F) = 1
 - path là chuỗi của những vertex được connect với nhau. Ví dụ: A -> B -> D -> C -> F
 - path length là số lượng edges được connect trong path
 - cycle là một cái path, tuy nhiên điểm bắt đầu và kết thúc là một vertex. Ví dụ: A -> B -> D -> C -> A
 - 1 cái cycle bất kì là path những không phải cái path nào cũng là cycle
![image](https://github.com/oxygen-batd/oxyGraph/assets/167840668/9b0222ec-c4b6-4b2f-b922-8af8db8434f2)

![image](https://github.com/oxygen-batd/oxyGraph/assets/167840668/adac7b7d-763b-4976-8463-ad43c4638667)


## Chuyển đổi Graph vào code
- Cách 1: Chuyển đổi thành mảng 2 chiều (matrix). Với giá trị [x][y] = nếu có connect thì là 0, không là 1.
  ![image](https://github.com/oxygen-batd/oxyGraph/assets/167840668/58b8f2ee-7558-4632-9e89-654e8f2389a7)

- Cách 2: Edge set - Danh sách của connection

- Cách 3: Dùng Hashtable. Với Key là vertex còn value là các neighbors
  ![image](https://github.com/oxygen-batd/oxyGraph/assets/167840668/64de5a2f-0954-49be-bd1a-c88e16632f7c)
