-- // ========================================
-- // L.7 - Custom Loader & Advanced Script
-- // ========================================

local Players = game:GetService("Players")
local localPlayer = Players.LocalPlayer

-- رسالة ترحيبية وتأكيد عمل السكربت في الكونسول
print("----------------------------------------")
print(" [L.7 Hub] Script loaded successfully!")
print(" Player: " .. tostring(localPlayer.Name))
print("----------------------------------------")

-- يمكنك إضافة الأوامر أو الواجهة الخاصة بك هنا
local success, err = pcall(function()
    -- مكان تنفيذ الأكواد الأساسية للسكربت
    print("Executing L.7 script functions...")
end)

if not success then
    warn("Error executing L.7 script: " .. tostring(err))
end
