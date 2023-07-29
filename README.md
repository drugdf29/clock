# clock
import time

def focus_clock(duration):
    seconds = duration * 60
    while seconds > 0:
        minutes, secs = divmod(seconds, 60)
        timer_display = f"{minutes:02d}:{secs:02d}"
        print(timer_display, end='\r')
        time.sleep(1)
        seconds -= 1

    print("专注结束！")

if __name__ == "__main__":
    focus_duration = 25  # 专注时长（分钟）
    focus_clock(focus_duration)
