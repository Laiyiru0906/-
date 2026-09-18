# -

def score_calculator():
scores = []

print("=== 考試成績平均計算器 ===")
print("提示：輸入成績後按 Enter，全部輸入完畢請輸入 'q' 結束計算。\n")

while True:
    user_input = input("請輸入成績（或輸入 'q' 結算）：").strip()

    # 輸入 q 或 Q 代表結束輸入
    if user_input.lower() == "q":
        break

    # 錯誤處理與分數計算
    try:
        score = float(user_input)

        # 限制分數合理的範圍 (0~100)
        if score < 0 or score > 100:
            print("⚠️ 請輸入有效分數（範圍應在 0 到 100 之間）")
            continue

        scores.append(score)
        print(f"已記錄分數：{score}")

    except ValueError:
        print("⚠️ 請輸入有效分數")

# 計算輸出結果
print("\n-------------------------")
if scores:
    average = sum(scores) / len(scores)
    print(f"共輸入 {len(scores)} 筆成績")
    print(f"所有成績：{scores}")
    print(f"平均分數為：{average:.2f} 分")
else:
    print("未輸入任何有效成績。")

if name == "main":
score_calculator()
