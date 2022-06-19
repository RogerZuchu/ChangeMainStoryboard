# ChangeMainStoryboard



# Step 1 
<img width="1680" alt="Screenshot 2022-06-19 at 17 06 38" src="https://user-images.githubusercontent.com/107794765/174477147-ad959048-7db8-4498-94a4-94313402fd6a.png">


# Step 2
<img width="1680" alt="Screenshot 2022-06-19 at 17 10 21" src="https://user-images.githubusercontent.com/107794765/174477155-acc359a2-c3d9-48e4-b9c8-3bea3b10642d.png">


# Step3 
<img width="1680" alt="Screenshot 2022-06-19 at 17 27 28" src="https://user-images.githubusercontent.com/107794765/174477157-c551595c-e817-4984-972e-f4421319dd70.png">


# Step 4  Use Extension UIViewController tự viết

``extension UIViewController{
            func directionToViewController(nameStoryboard:String,withIdentifier:String){
                let storyboard = UIStoryboard(name: nameStoryboard, bundle: nil)
                let gotoNextStoryboard = storyboard.instantiateViewController(withIdentifier: withIdentifier) as! UIViewController
                self.navigationController?.pushViewController(gotoNextStoryboard, animated: true)
            }
}``

<img width="1680" alt="image" src="https://user-images.githubusercontent.com/107794765/174477975-26d9cea1-4b91-4c48-98a3-804205089ae8.png">


# Step 5 Add withIdentifier trong extension ở Storyboard ID trong Storyboard mà mình muốn chuyển tới
<img width="1680" alt="Screenshot 2022-06-19 at 17 52 54" src="https://user-images.githubusercontent.com/107794765/174477867-6d16ed24-edae-4a96-9da6-c638970760f0.png">


# Step 6 Tạo UIViewController để viết code chuyển navController



``class AnotherVC:UIViewController{
    @IBAction func gotoMainVC(_ sender: UIButton) {
        self.directionToViewController(nameStoryboard: "MainVC", withIdentifier: "MainVC")
    }
    override func viewDidLoad() {
        super.viewDidLoad()
     
    }
}``

<img width="1680" alt="Screenshot 2022-06-19 at 18 08 03" src="https://user-images.githubusercontent.com/107794765/174477953-2c710c35-ddc3-44c2-93e5-c7da67beaf9f.png">
