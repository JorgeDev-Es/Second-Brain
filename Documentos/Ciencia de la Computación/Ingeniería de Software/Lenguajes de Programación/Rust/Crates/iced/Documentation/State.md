# iced State
In Rust, given the ownership and borrowing rules, it is extremely important to think carefully about the data model of your application.
In Iced, the `State` of your application is typically managed within your main application struct.
This struct holds all the data that your UI needs to render and interact with.