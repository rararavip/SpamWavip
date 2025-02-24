import pyautogui
import time
from warnings import warn

def send_whatsapp_message():
    # تحذير بشأن الاستخدام المكثف
    warn("إرسال الرسائل بشكل متكرر قد يتسبب في حظر واتساب!", UserWarning)
    
    phone_number = input("أدخل رقم الهاتف (مع رمز الدولة): ")
    message = input("أدخل الرسالة: ")
    
    try:
        while True:
            # فتح علامة تبويب جديدة في المتصفح (يتطلب Chrome)
            pyautogui.hotkey('ctrl', 't')
            
            # الذهاب إلى واتساب ويب
            pyautogui.write('https://web.whatsapp.com/send?phone=' + phone_number)
            pyautogui.press('enter')
            time.sleep(15)  # انتظر تحميل واتساب ويب
            
            # كتابة الرسالة وإرسالها
            pyautogui.write(message)
            pyautogui.press('enter')
            
            # إغلاق التبويب بعد الإرسال
            pyautogui.hotkey('ctrl', 'w')
            
            time.sleep(1)  # انتظر ثانية قبل إعادة الإرسال
            
    except KeyboardInterrupt:
        print("\nتم إيقاف البرنامج.")

if __name__ == "__main__":
    send_whatsapp_message()
