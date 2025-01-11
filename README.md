local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "레전드 허브브",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "로딩중...",
   LoadingSubtitle = "by 스팅",
   Theme = "Default", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = false,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "스팅의 스크립트 Hub",
      Subtitle = "환영합니다!",
      Note = "키 : sting", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"sting"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local MainTab = Window:CreateTab("메인 탭", nil) -- Title, Image
local MainSection = MainTab:CreateSection("스크립트")

Rayfield:Notify({
   Title = "실행중",
   Content = "맵 뿌시러 가자!!",
   Duration = 6.5,
   Image = 4483362458,
})

local Button = MainTab:CreateButton({
   Name = "어드민 스크립트",
   Callback = function()
   loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "쌈뽕타워",
   Callback = function()
   loadstring(game:HttpGet("https://pastebin.com/raw/BEVRPYjM"))()
   end,
})

local MainSection = MainTab:CreateSection("이외 허브")

local Button = MainTab:CreateButton({
   Name = "핵선생님 허브",
   Callback = function()
  loadstring(game:HttpGet("https://raw.githubusercontent.com/hack999hack999px/hack999hack999px/refs/heads/main/%40로블록스-핵-선생님의-스크립트-모음집-hub.txt"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "EZ한 허브",
   Callback = function()
   loadstring(game:HttpGet("https://pastebin.com/raw/uqQHvSDJ"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "개트롤 허브",
   Callback = function()
   loadstring(game:HttpGet("https://pastefy.app/JjlESrvw/raw"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "즐겜 허브",
   Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/siwon2da/siwon2dac/refs/heads/main/v5"))()
   end,
})

local Button = MainTab:CreateButton({
   Name = "스팅 허브",
   Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/ss73667366/sting-hub/main/README.md"))()
   end,
})

local MainSection = MainTab:CreateSection("조작")

local Slider = MainTab:CreateSlider({
   Name = "스피드",
   Range = {1, 300},
   Increment = 1,
   Suffix = "속도",
   CurrentValue = 16,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value 
   end,
})

local Slider = MainTab:CreateSlider({
   Name = "점프파워",
   Range = {1, 500},
   Increment = 1,
   Suffix = "점프력",
   CurrentValue = 16,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
   end,
})
