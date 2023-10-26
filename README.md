# Data_Analytics_Quizz_1
პროექტი წარმოადგენს Stack Overflow-ს 2023 წლის გამოკითხვის შედეგების მონაცემთა ანალიზს. პროგრამა შესრულებულია python პროგრამირების ენისა და jupyter notebook-ის გამოყენებით. 2023 წლის გამოკითხა შეგიძლიათ იხილოთ მოცემულ ბმულზე
https://survey.stackoverflow.co/2023/

# პროგრამის მუშაობის პროცესის აღწერა
ხდება survey_results_public.csv ფაილიდან მონაცემთა წაკითხვა და მონაცემებზე ინფრომაციის გაგება: ცხრილის ზომები, სვეტების დასახელებები, თითოეული სვეტის ტიპის გაგება. 

# ცხრილიდან სასურველი სტრიქონების და სვეტების გამოტანა. 
* ცხრილიდან გამობეჭდილია:
* პირველი 3 სტრიქონი;
* ბოლო 4 სტრიქონი;
* სვეტი განათლების დონის შესახებ;
* პირველი სტრიქონის ასაკობრივი კატეგორია;
* შესაბამისად ინდექსად 0, 50, 12 და 50 რესპოდენტებისს განათლების დონე, კოდის სწავლის სტილი, პროგრამირების წლების რაოდენობა და პროგრამული ენები;
* ინდექსათ 2 რესპოდენტის სამუშაო განაკვეთის გამოტანა;
* ინდექსად 100, 705, 1399 მომხმარებლების ასაკობრივი რეინჯის, პროგრამული აქტივობების, იმ პროგრამირების ენების რომელზეც ამ დველოპერს აქვს ნამუშევარი და ხელფასი;

  
# ინდექსირების დანიშვნაა
პირველ რიგში გადავხედით არსებულ სვეტებს. როგორც იკვეთება ResponseId სუკეთესო სვეტია ინდექსირებისთვის და ამიტომ დავნიშნოთ იგი. როდესაც ცხრილს წავიკითხავთ 
აშკარაა, რომ ResponseId  არის ინდექსი, რადგანაც იგი გამუქბულია და სხვა სვეტების გასწვრივ არაა ამ სვეტის დასახელება.
რადგან ResponseId იწყება 1-დან, ამიტომ ამ შემთხვევაში ინდექსი შეესაბამება პოზიციონირებას, რაც მუშაობას უფრო მოხერხებულს ხდის.
მონაცემები გადავალაგეთ ინდექსის კლების მიხედვით და დავასეივეთ. შემდეგ ისევ ზრდადოებით დავალაგეთ და ესეც დავასეივეთ.


# 2 პარამეტრზე დამოკიდებული ფილტი
შევქმენით 2 პარამეტრზე დამოკიდებული ფილტრი, რათა გამოვტანოტ იმ დეველოპერთა პროგრამული აქტივობების, პროგრამული ენებისა
და ანაზღაურებები, რომლებითა ანაზღაურება მეტია 100,000-ზე და ფლობენ C# პროგრამირების ენას.

# ცხრილი სორტირება 2 პარამეტრის გამოყენებით
ცხრილს ვალაგებთ პირველ რიგში განადლების დონის (EdLeve) ლექსიკოგრაფიული ზრის მიხედვით და შემდეგ სამუშაო გამოცდილების (WorkExp) კლების მიხედვით. შემდგომ ვბეჭდავთ ამ სორტირების
შედეგად შეცვლილ ცხრილს.

# სტატისტიკური ფუნქციები
სამუშაო გამოცდილების (WorkExp) სვეტისთვის გამოყენებულია სხვადასხვა სტატისტიკური ფუნქციები:
* საშუალო 11.405126322311204
* მინიმაუმი 0
* მაქსიმუმუ 50
* სტანდარტული გადახრა 9.05198941848756
* მედიანა 9

# დიაგრამების აგება
სულ აგებულია 3 დიაგრამა
1) ჰორიზონტალური სვეტოვანი დიაგრამა - გამოკითხულთა ასაკობრივი კატეგორიების პროცენტულების მიხევით.
2) წრიული დიაგრამა - თუ რამდენი პროცენტი იყენებს ხელოვნური ინტელექტის თულებს; რამდენი გეგმავს რომ გამოიყენებს და რამდენი აცხადებს უარს მის გამოყენებაზე.
3) ვერტიკალური სვეტოვანი დიაგრამა - რამოდენიმე ამორჩეული კურსის პლატფორმა და მათი გამოყენების პროცენტულობა



# გამოყენებული ბიბლიითეკები/თულები:
pandas, numpy, matplotlib

# მნიშვნელოვანი ინფორმაცია
github-ის მიერ დაწესებული მოცულობითი შეზღუდვის გამო, სამწუხაროდ ვერ მოხერხდა survey_results_public.csv ფაილის ატვირთვა, თუმცა მისი გადმოწერა მარტივად შეგიძლიათ
მოცემული ბმულზე დაწკაპებით
https://cdn.stackoverflow.co/files/jo7n4k8s/production/49915bfd46d0902c3564fd9a06b509d08a20488c.zip/stack-overflow-developer-survey-2023.zip
