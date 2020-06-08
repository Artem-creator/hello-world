import Foundation
var rightAnswer: String?
var no: Optional<String> = "n"
repeat {
let randonNumber = UInt8(arc4random_uniform(50))
print("Компьютер загадал число, отгадай его.")
var myNumber: String?
repeat {
    print("Введите число и нажмите Enter")
    myNumber = readLine()
    if (UInt8(myNumber!)! == randonNumber){
        print("Вы угадали")
    }else if (UInt8(myNumber!)! < randonNumber) {
        print("Ваш вариант меньше загаданного!")
    } else if (UInt8(myNumber!)! > randonNumber) {
        print("Ваш вариант больше загаданного")
    }
} while randonNumber != UInt8(myNumber!)
print("Хотите попробовать еще раз? y/n?")
rightAnswer = readLine()
} while rightAnswer! != no!
