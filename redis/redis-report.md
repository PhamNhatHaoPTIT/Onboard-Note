## Week 8 - Redis

### Time 11/11 -> 15/11

+ Cho service A cung cấp API ping, đồng thời có 1 counter để đếm số lần gọi của API này, mỗi lần api này đc gọi a tăng counter này lên, định kì mỗi 5 phút a cập nhật counter này xuống DB

+ Deploy service này với 2 instances, implement hàm ping sau cho phần counter luôn đếm đúng số lần gọi