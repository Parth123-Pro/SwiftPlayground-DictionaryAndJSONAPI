# SwiftDictionary
<img width="1167" alt="Screenshot 2022-11-20 at 9 17 21 PM" src="https://user-images.githubusercontent.com/55745745/202911712-5c41cd8a-c03c-4aeb-bb40-724c28d3049d.png">
<img width="1300" alt="Screenshot 2022-11-20 at 11 56 40 PM" src="https://user-images.githubusercontent.com/55745745/202919312-7ec255ee-b4f9-4d53-90d8-cccb1ebbfc8a.png">
<hr>
## OR
<hr>

<img width="785" alt="Screenshot 2022-11-21 at 12 02 08 AM" src="https://user-images.githubusercontent.com/55745745/202919738-9e282d06-3fd6-4b3b-8a97-34201735d9d1.png">
import UIKit<br>
class ViewController: UIViewController {<br>
override func viewDidLoad() {<br>
super.viewDidLoad()<br>
let path = Bundle.main.path(forResource: "colors", of Type: "json")<br>
let url = URL (fileURLWithPath: path!)<br>
do {<br>
let data = try Data (contentsOf: url)<br>
let colors = try JSONDecoder().decode([String: [Int]].self, from: data)<br>
print (colors)<br>
}<br>
catch {}<br>
}<br>
} <br>
