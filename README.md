- 👋 Hi, I’m @hzubovich
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
hzubovich/hzubovich is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
public class Cases {
    public abstract class Case {
        private final int lig;
        private final int col;
        public abstract boolean estLibre();

        public Case (int lig, int col) {
            this.lig = lig;
            this.col = col;
        }

        public int getCol() {
            return col;
        }

        public int getLig() {
            return lig;
        }
    }

    public abstract class Entite {
        public int resistance;
        public abstract String toString(String background);

        public Entite (int resistance) {
            this.resistance = resistance;
        }

        public int getResist() {
            return resistance;
        }

        public void setResist(int resistance) {
            this.resistance = resistance;
        }
    }

    public class CaseTraversable extends Case {
        private Entite contenu;

        public CaseTraversable (int lig, int col) {
            super(lig, col);
            contenu = null;
        }

        public Entite getContenu() {
            return contenu;
        }

        public void vide() {
            contenu = null;
        }
         
        public void entre(Entite e) {
            if (contenu == null) {
                contenu = e;
            } else {
                throw new IllegalStateException("dolboeb");
            }
        }
    }

    public class CaseIntraversable extends CaseTraversable {
        public CaseIntraversable (in lig, int col) {
            super (lig, col);
        }
        public boolean estLibre() {
            return super.estLibre;
        }
    }
}
