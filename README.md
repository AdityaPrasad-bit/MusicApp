# MusicApp

Hi everyone how are you ?
Hope you are doing well.

I have created another app and it is xylophone app. 

I have learnt so many things like what is dispatch queue and what it is use for. How to change the opacity of the button. How to animate the button.
How to work with AVFoundation to play the sound on the phone.

For animating the button this is the code:-

 UIView.animate(withDuration: 0.3) {
        sender.alpha = 0.5
    }

    DispatchQueue.main.asyncAfter(deadline: .now() + 0.3 ) {
        UIView.animate(withDuration: 0.3) {
            sender.alpha = 1.0
        }
    }
    
asyncafter stops the execution after for a specifed amount of time.
Dispatch is code block which works on fifo based execution.
    
    
    
 For playing the sound:
  let url = Bundle.main.url(forResource: soundName, withExtension: "wav")
  player = try! AVAudioPlayer(contentsOf: url!)
  player.play()
    
Bundle→ A representation of the code and resources stored in a bundle directory on disk.
Main → is basically use to locate the sound file resource
It is basically doing to locate the resouces C.wav which is present in the project→ sound Folder where it is declare in our project.

![Simulator Screen Shot - iPhone 13 Pro Max - 2022-02-10 at 09 21 06](https://user-images.githubusercontent.com/85185631/153339269-cd78d723-fa23-42cc-9149-1a4272b7e850.png)




https://user-images.githubusercontent.com/85185631/153339293-58f43a4e-de6e-422e-b81f-f5bab6f74889.mp4

Download the project and you will hear the sounds
