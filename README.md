# Prework
import SwiftUI

struct ContentView: View {
    @State private var backgroundColor = Color.white

    var body: some View {
        VStack(spacing: 20) { // Arrange items vertically with spacing
            Text("Abdulahi Jilal Hirsi") // First Label
                .font(.title)
            
            Text("University of washington Bothell") // Second Label
                .font(.headline)
            
            Text("Aerospace engineering") // Third Label
                .font(.subheadline)
                .fontWeight(/*@START_MENU_TOKEN@*/.bold/*@END_MENU_TOKEN@*/)
                .foregroundColor(Color.yellow)
                
            func changeColor() -> UIColor{

                    let red = CGFloat.random(in: 0...1)
                    let green = CGFloat.random(in: 0...1)
                    let blue = CGFloat.random(in: 0...1)

                    return UIColor(red: red, green: green, blue: blue, alpha: 0.5)
                }

                    
                }

            }
            Button(action: {
                // Action to change background color to a random color
                backgroundColor = Color(
                    red: .random(in: 0...1),
                    green: .random(in: 0...1),
                    blue: .random(in: 0...1)
                )
            }) {
                Text("Change Background Color") // Button label
                    .padding()
                    .background(Color.blue)
                    .foregroundColor(.white)
                    .cornerRadius(10)
            }
        }
        .padding()
        .background(backgroundColor)
        .edgesIgnoringSafeArea(.all) // Make the background color fill the whole screen
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}

