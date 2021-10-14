# `self` Discussion Questions

## Instructions

Take 30 minutes and answer the following questions together with your group. Take turns playing around with the code provided in Pry or IRB.

![](https://curriculum-content.s3.amazonaws.com/module-1/discussion-questions/using-self-in-ruby/Image_110_%20FunnyRobots.png)

1 .   

      class FunnyBots  

        attr_accessor :name, :quotes  

        @@bots = []

        def initialize(name, quotes)
          @name = name
          @quotes = quotes
          @@bots << self
        end

       def random_quote
          self.quotes.sample
        end

        def self.bots
          @@bots
        end

    end

      archer = FunnyBots.new("Archer", ["Q: How did the programmer die in the shower? A:He read the shampoo bottle instructions: Lather. Rinse. Repeat. ", "A UI is like a joke. If you have to explain it, it's not good.", "Q: How many programmers does it take to change a light bulb? A: None – It’s a hardware problem"] )

  A. What is **self** in this line ```@@bots << self``` ?  
  B. What is **self** in this line ```self.quotes.sample```?  
  C. What kind of **method** is `self.bots` & what is **self**? 
  D. Will this work ```archer.bots```? Why / why not? 

2 .

![](https://curriculum-content.s3.amazonaws.com/module-1/discussion-questions/using-self-in-ruby/Image_111A_Photo%20by%20C%20Drying%20on%20Unsplash.png)

    class Bicycle

      attr_reader :tire

        def initialize(tire, gears, style)
          @tire = tire
          @gears = gears
          @style = style
        end

        def tire_size
          self.tire
        end

        def self.gears
          @gears
        end

    end

    mongoose = Bicycle.new(4, 10, "BMX")

  For what reasons will the following method calls fail : ```mongoose.tire_size = 5```, ```mongoose.gears```, ```Bicycle.bikes```, ```Bicycle.styles```? Restructure the class to fix the issues.


