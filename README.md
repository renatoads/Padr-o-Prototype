package prototype;

public abstract class Animal implements Cloneable {
	
	String animalNome;
	
	public void setNomeAnimal (String animalNome) {
		this.animalNome = animalNome;
	}
	
	public String getNomeAnimal() {
		return this.animalNome;
	}
	
	public void comer() {
		System.out.println(animalNome + "está comendo...");
	}
	
	public void andar() {
		System.out.println(animalNome + "está andando...");
	}
	
	@Override
	public Object clone() {
		Object object = null;
		try {
			object = super.clone();
		}catch (CloneNotSupportedException exception) {
			System.out.println("A ovelha não foi clonada");
		}
		return object;		
		
	}
}
