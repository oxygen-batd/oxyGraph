# Maths

1. Việc kiểm tra xem có tồn tại kết nối giữa hai đỉnh (nodes) trong một đồ thị hay không là một vấn đề cơ bản trong lý thuyết đồ thị
- Thuật toán Depth-First Search (DFS):
  + Bắt đầu từ đỉnh xuất phát, thực hiện DFS.
  + Đánh dấu điểm đã ghé thăm
  + Nếu gặp đỉnh đích trong quá trình duyệt thì trả về True
  + Nếu không thì dùng DFS duyệt hết các đỉnh kề
  + Nếu duyệt hết mà không tìm thấy thì trả về False

![image](https://github.com/oxygen-batd/oxyGraph/assets/167840668/c747af05-5837-4837-a082-e06e50be09ed)

- Code:
  ```
   function dfs(start, end, visited = {}, checkFirstVertex) {
    if (!checkFirstVertex && start === end) return true;

    visited[start] = true;
    const neighbors = graph.getNeighbors(start); // graph.adjacencyList.get(start);
    for (let neighbor of neighbors) {
        if (!visited[neighbor]) {
            if (dfs(neighbor, end, visited, false)) return true;
        }
    };
    return false;
  }
