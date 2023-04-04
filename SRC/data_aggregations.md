You will aggregate the data for extracting insights. 

Do the following steps:
1. Create 2 tables. 
![1 0-Create table sales](https://user-images.githubusercontent.com/128261514/229657772-3a2776c3-fbb5-43c1-843d-4795df0f551f.png)
![1 0-Select table sales](https://user-images.githubusercontent.com/128261514/229657774-864a2324-3423-4465-a2a8-a140b4c2e531.png)

 - The first table shows the average critic score for Sports games.  Store this information in a column called “sports_critic_score”.  

To create a table for the average critic score of sports games:
```
CREATE TABLE avg_sports_critic_score AS 
SELECT AVG(Critic_Score) AS sports_critic_score
FROM sales
WHERE Genre = 'Sports';
```
 ![1 1-Create table avg sports critic score](https://user-images.githubusercontent.com/128261514/229657782-22ba2077-9405-497e-884c-f1d319ef4fd0.png)
 ![1 1-Select table avg sports critic score](https://user-images.githubusercontent.com/128261514/229657783-00895438-3bbb-442d-b9a7-58595d4c45b0.png)

 - The second table shows the average critic score for Shooter games.  Store this information in a column called “shooter_critic_score”.

To create a table for the average critic score of shooter games:
```
CREATE TABLE avg_shooter_critic_score AS 
SELECT AVG(Critic_Score) AS shooter_critic_score
FROM sales
WHERE Genre = 'Shooter';
```
 ![1 2-Create table avg shooter critic score](https://user-images.githubusercontent.com/128261514/229657792-0178b3d7-a51b-45a6-8ec8-ec72c0424368.png)
 ![1 2-Select table avg shooter critic score](https://user-images.githubusercontent.com/128261514/229657794-a8c6b23e-8890-484a-b7dc-6f7cea269cb3.png)

2. Create 3 statistics tables (average, min, max) for the global_sales for:  all games, Sports games, Shooter games. For each table, label the columns as: “average_global_sales”, “min_global_sales”, and “max_global_sales”.

To create a table for global sales and count of games for sports games:
```
CREATE TABLE count_sports_games_global_sales AS
SELECT SUM(Global_Sales) as global_sales,
       COUNT(*) as count
FROM sales
WHERE Genre = 'Sports';
```
![2 1-Create table stats all games global sales](https://user-images.githubusercontent.com/128261514/229657890-5355d949-ee54-4a97-951a-f1f918ed7364.png)
![2 1-Select table stats all games global sales](https://user-images.githubusercontent.com/128261514/229657893-b71b7c18-ee54-48b2-8b2f-ac023247891e.png)
![2 2-Create table stats sports global sales](https://user-images.githubusercontent.com/128261514/229657894-217a492b-3280-4764-81f1-1f6a18befa35.png)
![2 2-Select table stats sports global sales](https://user-images.githubusercontent.com/128261514/229657896-e6f9b6f2-393a-41e3-8f78-549b718ad42f.png)
![2 3-Create table stats shooter global sales](https://user-images.githubusercontent.com/128261514/229657900-b6a03d66-f4a3-4a7f-a3d2-777a4311826d.png)
![2 3-Select table stats shooter global sales](https://user-images.githubusercontent.com/128261514/229657901-7372530a-156d-4b6c-9ae0-9c2a80af272a.png)


3. Create 2 tables containing the global_sales and the count of games with that global_sales for: Sports games and Shooter games.  For each table, label the columns as: “global_sales” and “count”.

To create a table for global sales and count of games for sports games:
```
CREATE TABLE count_sports_games_global_sales AS
SELECT SUM(Global_Sales) as global_sales,
       COUNT(*) as count
FROM sales
WHERE Genre = 'Sports';
```

To create a table for global sales and count of games for shooter games:
```
CREATE TABLE count_shooter_games_global_sales AS 
SELECT SUM(Global_Sales) as global_sales,
       COUNT(*) as count
FROM sales
WHERE Genre = 'Shooter';
```

![3 2-Select table count shooter global sales](https://user-images.githubusercontent.com/128261514/229657936-c31c2f15-f5b5-4ebb-b38a-6eb94a3f90ae.png)
![3 1-Create table count sports global sales - NEW](https://user-images.githubusercontent.com/128261514/229657942-a77188e7-1b84-4114-9c56-f95c2516c999.png)
![3 1-Create table count sports global sales](https://user-images.githubusercontent.com/128261514/229657947-a3828df4-8550-4489-bedd-73ffabb1da6d.png)
![3 1-Select table count sports global sales - NEW](https://user-images.githubusercontent.com/128261514/229657949-a025458e-c851-40c4-bae4-235301751b21.png)
![3 1-Select table count sports global sales](https://user-images.githubusercontent.com/128261514/229657952-1b9080f7-347c-4a91-9537-e3bb05c7d4fb.png)
![3 2-Create table count shooter global sales - NEW](https://user-images.githubusercontent.com/128261514/229657955-eb408155-d202-430c-beab-f691714e53b1.png)
![3 2-Create table count shooter global sales](https://user-images.githubusercontent.com/128261514/229657959-d4955b49-71b0-4bb2-b1a1-0801814d1ec1.png)
![3 2-Select table count shooter global sales - NEW](https://user-images.githubusercontent.com/128261514/229657963-26750a10-b0d3-4c32-840f-a7f443a3eba5.png)
