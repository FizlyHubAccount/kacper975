local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "Fizly Hub Key System (tds) ", HidePremium = false,IntroText = "Fizly Hub Key System(tds) ", SaveConfig = true, ConfigFolder = "Fizly hub Key System(tds)"})
--loading 
if game.PlaceId == 3260590327 then
  OrionLib:MakeNotification({
    Name = "Correct",
    Content = "You are in correct game pls wait",
        Image = "rbxassetid://4483345998",
    Time = 5
  })
  wait(4)


           OrionLib:MakeNotification({
	Name = "Logged in!",
	Content = "You are logged in as "..Player.Name..".",
    	Image = "rbxassetid://4483345998",
	Time = 5
})
--keys
_G.Key = "5368566D59713374"
_G.KeyInput = "3F4528482B4D6250"

--Main function

function load()
	local Window2 = OrionLib:MakeWindow({Name = "Fizly  Hub (tds) ", HidePremium = false,IntroText = "Fizly Hub (tds)", SaveConfig = true, ConfigFolder = "Fizly  Hub (TDS)"})
	--Main
	local Main = Window2:MakeTab({
		Name = "Main",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
	
  })
  --MultiStrats
  local MultiStrats = Window2:MakeTab({
		Name = "MultiStrats",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
  --Strats
  local Strats = Window2:MakeTab({
		Name = "Strats",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
--Super op strats
  local OpStrats = Window2:MakeTab({
		Name = "Super op strats",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
  --Soon1
  local Soon1 = Window2:MakeTab({
		Name = "Soon",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
  --Soon2
  local Soon2 = Window2:MakeTab({
		Name = "Soon 2",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
  --Credits End
  local Credits = Window2:MakeTab({
		Name = "Credits",
		Icon = "rbxassetid://4483345998",
		PremiumOnly = false
  })
  Credits:AddParagraph("Credits to: Time Fixty v.1.4 is soon")
 
       coroutine.resume(NotificationCoroutine)
        
       OrionLib:Init()
        
       task.wait(2)


end
--function

function CorrectKeyNotification()
    OrionLib:MakeNotification({
  Name = "Correct Key!",
  Content = "You have entered the correct key!",
  Image = "rbxassetid://4483345998",
  Time = 5
    })
end


 



function InCorrectKeyNotification()
    OrionLib:MakeNotification({
  Name = "InCorrect Key!",
  Content = "You have entered the Incorrect key!",
  Image = "rbxassetid://4483345998",
  Time = 7
    })
end

function GetKeyNotifiation()
    OrionLib:MakeNotification({
  Name = "Get Key Link!",
  Content = "Get Key on Discord: soon",
  Image = "rbxassetid://4483345998",
  Time = 7
    })
end

function HowToGetKeyNotifiation()
    OrionLib:MakeNotification({
  Name = "Here how you can key",
  Content = "Get Key on Discord: ",
  Image = "rbxassetid://4483345998",
  Time = 7
    })
end
--tab and more
local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local TabGet = Window:MakeTab({
	Name = "Get Key Here",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Enter Key ",
	Default = "",
    TextDisappear = true,
	Callback = function(Value)
		_G.KeyInput = Value
	end    
})

TabGet:AddButton({
	Name = "Get link to key",
	Callback = function()
		HowToGetKeyNotifiation()

	end
		
		})
		

Tab:AddButton({
	Name = "Check Key",
	Callback = function()
        if _G.KeyInput == _G.Key then
               load()
			CorrectKeyNotification()


		


           
        else

            InCorrectKeyNotification()
        end
      		
  	end    
})

  else
  OrionLib:MakeNotification({
  Name = "Error",
  Content = "The game is incorrect",
  Image = "rbxassetid://4483345998",
  Time = 7
  
 
  })
  
  wait(2)
  
       OrionLib:MakeNotification({
	Name = "Warning",
	Content = "Gui will be destroy in 6 second ",
	Image = "rbxassetid://4483345998",
	Time = 5
       })
    wait(6)
       
        OrionLib:Destroy()
       end 
             
       OrionLib:Init()
