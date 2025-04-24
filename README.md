- 👋 Hi, I’m @roy990525
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
roy990525/roy990525 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
SELECT u.nickname, SUM(b.damage) AS total_damage
FROM battle_logs b
JOIN users u ON b.user_id = u.user_id
WHERE battle_time >= CURRENT_DATE - INTERVAL '30 days'
GROUP BY u.nickname
ORDER BY total_damage DESC
LIMIT 10;

