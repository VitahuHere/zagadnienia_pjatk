### **Testowanie hipotez statystycznych**  

**Testowanie hipotez** to metoda statystyczna służąca do oceny, czy dostępne dane dostarczają wystarczających dowodów do odrzucenia pewnej założonej hipotezy na określonym poziomie istotności.  

### **Podstawowe pojęcia**  

1. **Hipoteza zerowa ($H_0$)**  
   - Jest to założenie, które testujemy, często oznacza brak efektu lub brak różnicy.  
   - Przykład: "Średni wzrost mężczyzn i kobiet jest taki sam".  

2. **Hipoteza alternatywna ($H_1$ lub $H_A$)**  
   - Przeciwieństwo hipotezy zerowej, wskazuje na istnienie efektu lub różnicy.  
   - Przykład: "Średni wzrost mężczyzn i kobiet różni się".  

3. **Poziom istotności ($\alpha$)**  
   - Prawdopodobieństwo popełnienia błędu I rodzaju (odrzucenie prawdziwej hipotezy zerowej).  
   - Najczęściej przyjmowane wartości: **0.05** (5%) lub **0.01** (1%).  

4. **Wartość p (p-value)**  
   - Prawdopodobieństwo uzyskania wyników co najmniej tak ekstremalnych jak zaobserwowane, zakładając, że $H_0$ jest prawdziwa.  
   - Jeśli $ p \leq \alpha $, odrzucamy $ H_0 $, co oznacza, że wyniki są **statystycznie istotne**.  

---

### **Rodzaje błędów w testowaniu hipotez**  

- **Błąd I rodzaju** ($\alpha$) – odrzucenie prawdziwej hipotezy zerowej (fałszywe odkrycie).  
- **Błąd II rodzaju** ($\beta$) – nieodrzucenie fałszywej hipotezy zerowej (przeoczenie efektu).  

---

### **Przykład testu hipotez**  

Załóżmy, że producent leków chce sprawdzić, czy nowy lek obniża ciśnienie krwi bardziej niż standardowy lek.  

1. **Hipotezy:**  
   - $H_0$: Nowy lek nie obniża ciśnienia krwi skuteczniej niż standardowy.  
   - $H_A$: Nowy lek obniża ciśnienie bardziej niż standardowy.  

2. **Zbieramy dane**: Mierzymy ciśnienie pacjentów po zastosowaniu obu leków.  

3. **Wybieramy test statystyczny**: Możemy użyć testu t-Studenta dla dwóch niezależnych grup.  

4. **Obliczamy wartość p**: Jeśli $ p \leq 0.05 $, odrzucamy $ H_0 $ i uznajemy, że nowy lek działa lepiej.  

---

### **Rodzaje testów statystycznych**  

- **Test t-Studenta** – porównuje średnie dwóch grup.  
- **Test chi-kwadrat** – bada zależności między dwiema zmiennymi kategorycznymi.  
- **ANOVA** – porównuje średnie więcej niż dwóch grup.  
- **Test U Manna-Whitneya** – test nieparametryczny dla dwóch niezależnych grup.  

Testowanie hipotez jest kluczową metodą w analizie danych, medycynie, ekonomii i wielu innych dziedzinach nauki.