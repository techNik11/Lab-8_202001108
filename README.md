IT314 
SOFTWARE ENGINEERING

Lab-08

Name: Nikhil J Jethanandani
ID: 202001108
Date: 19-04-2023

SCREENSHOTS


CODE 

BoaTest.java

package Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {

	private Boa jen;
	private Boa ken;
	
	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy_1() {
		boolean output = ken.isHealthy();
		assertEquals(output,true);
	}
	
	@Test
	public void testIsHealthy_2() {
		boolean output = jen.isHealthy();
		assertEquals(output,false);
	}

	@Test
	public void testFitsInCage_1() {
		
		int cage = 4;
		boolean output = jen.fitsInCage(cage);
		assertEquals(output,true);
	}
	
	@Test
	public void testFitsInCage_2() {
		
		int cage = 4;
		boolean output = ken.fitsInCage(cage);
		assertEquals(output,true);
	}
	
	@Test
	public void testFitsInCage_3() {
		
		int cage = 6;
		boolean output1 = ken.fitsInCage(cage);
		assertEquals(output1,true);
	}
	
	@Test
	public void testFitsInCage_4() {
		
		int cage = 2;
		boolean output1 = ken.fitsInCage(cage);
		assertEquals(output1,false);
	}
	
	@Test
	public void lengthInInches_1() {
		
		
		int output1 = ken.lengthInInches();
		assertEquals(output1,36);
	}
	
	@Test
	public void lengthInInches_2() {
		
		
		int output1 = jen.lengthInInches();
		assertEquals(output1,24);
	}

}












