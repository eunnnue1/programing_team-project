# programing_team-project
# 감정별 다양한 키워드 조합을 딕셔너리로 작성
emotion_keywords = {
    "happy": ["기쁘다", "행복하다", "즐겁다", "좋다", "신난다", "뿌듯하다", "만족스러워", "기분좋아", "행복해", "웃겨"],
    "sad": ["슬프다", "우울하다", "눈물", "상심", "그립다", "속상해", "서운하다", "우울해", "외로워", "슬퍼","슬푸딩"],
    "angry": ["화난다", "짜증나", "분하다", "화가 난다", "짜증나요", "성질나", "불쾌해", "짜증나요", "화나요", "격분"],
    "fear": ["무섭다", "두렵다", "불안하다", "걱정돼", "겁이 나", "무서워", "불안해", "두려워", "겁나요", "불안해"],
    "surprise": ["놀라워", "깜짝", "엄청난", "신기하다", "놀랐다", "깜짝 놀랐어", "어머", "세상에", "와", "이럴수가"]
}

# 이모지 매핑 딕셔너리
emoji_map = {
    "happy": "😊",
    "sad": "😢",
    "angry": "😠",
    "fear": "😱",
    "surprise": "😲"
}

# 사용자로부터 입력 받기
user_input = input("상황을 입력하세요: ")

def analyze_emotion(text):
    text_lower = text.lower()
    for emotion, keywords in emotion_keywords.items():
        for keyword in keywords:
            if keyword in text_lower:
                return emoji_map[emotion]
    return "👉"  # 감정을 인식하지 못했을 때 기본 이모지

# 감정 분석 후 결과 출력
result = analyze_emotion(user_input)
print(f"입력하신 내용에 맞는 이모지: {result}")

import tkinter as tk

# 메인 윈도우 생성
root = tk.Tk()

# 윈도우 제목 설정
root.title("Tkinter 예시")

# 버튼 생성 및 배치
button = tk.Button(root, text="버튼 클릭")
button.pack()

# GUI 실행
root.mainloop()
