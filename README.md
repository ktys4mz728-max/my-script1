-- // ========================================
-- // L.7 - Ultimate Custom Script Hub
-- // Created exclusively for L.7
-- // ========================================

local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local localPlayer = Players.LocalPlayer

-- دالة إرسال إشعار داخل اللعبة (محمية بـ pcall لتفادي أي أخطاء)
local function sendNotification(title, text, duration)
    pcall(function()
        StarterGui:SetCore("SendNotification", {
            Title = title,
            Text = text,
            Duration = duration or 5,
        })
    end)
end

-- رسالة الترحيب في الكونسول
print("----------------------------------------")
print(" [L.7 Hub] Initializing script for: " .. tostring(localPlayer.Name))
print("----------------------------------------")

-- تشغيل الأوامر الأساسية بأمان تام (حماية pcall)
local success, err = pcall(function()
    -- [ هنا يقدر يوضع كود الوظائف أو الأزرار أو التعديلات المستقبلية ]
    print("L.7 Script executed successfully without errors.")
    
    -- إرسال إشعار مرئي أول ما يشتغل السكربت داخل اللعبة
    sendNotification("L.7 Hub", "تم تفعيل السكربت بنجاح، أهلاً بك يا L.7!", 6)
end)

if not success then
    warn("[L.7 Error]: Failed to execute main functions: " .. tostring(err))
    sendNotification("L.7 Error", "حدث خطأ بسيط أثناء تشغيل السكربت.", 5)
end

