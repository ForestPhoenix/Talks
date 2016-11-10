# Übersicht (für mich)

- OOP/MOP/PLOT/???
    - Nummer Ziehen in Ruby
    - mit mehreren threads
    - Wo sind Probleme
- FP
    - ein anderer Ansatz
    - Nummer Ziehen in Haskell
    - FP vs OOP

- Weitere Links
    - EWD

- Kritik am eigenen Vortrag (vllt?)
    - Problem als Beispiel zugeschnitten

# Ziehen einer Nummer in Ruby
```ruby
class Warteschalnge
    def initialize()
        @warteschalnge = []
    end

    def anstellen(kunde)
        @warteschalnge.push(kunde)
        self
    end

    def weiter()
        @warteschalnge.pop
    end      
end
```
