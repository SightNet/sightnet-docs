Итак, каждый пир имеет свою базу данных, локальный список репутации. И выступает одновременно в качестве сервера и клиента.

Когда пользователь вводит запрос -> пиры распространяют его с помощью gossip протокола. В течении 5 секунд пользователь будет ждать ответа от серверов, которые в ответ также отправят данные посредством gossip протокола с айди получателя результатов. Далее они ранжируются.