import re
from pynput.keyboard import Key, Controller, Listener

keyboard = Controller()

def process_key_press(key):

    key_text = re.sub(r"Key.|\'|\"", '', str(key))    
    if key_text == 'd':
        print('Corrected')
        keyboard.press(Key.backspace)
        keyboard.release(Key.backspace)
        keyboard.press(Key.shift)
        keyboard.press('x')
        keyboard.release('x')
        keyboard.release(Key.shift)

if __name__ == "__main__":
    listener = Listener(on_press=process_key_press)
    with listener :
        listener.join()
