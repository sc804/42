# general

###################
##    TESTERS    ##
###################

PrintftTester : #Tripouille
	git clone git@github.com:Tripouille/printfTester.git
	cd printfTester && make m
	cd ..
	rm -rf printfTester/

Tester-Santana : #ft_printf_tester
	git clone git@github.com:paulo-santana/ft_printf_tester.git
	cd ft_printf_tester && sh test m
	rm -rf ft_printf_tester

Tester-nmannage :
	curl -o test.c https://raw.githubusercontent.com/nmannage/printftester_mandatory/refs/heads/main/test.c
	make && cc test.c -L. -lftprintf -o test && ./test
	rm -rf test test.c


###################
##    TESTERS    ##
###################

so:				#this rule is necessary to run one of the libftTester
	$(CC) -nostartfiles -fPIC $(CFLAGS) $(SOURCES) $(BONUS)
	gcc -nostartfiles -shared -o libft.so $(OBJECTS) $(BONUS_OBJ)

libfterator :
	git clone git@github.com:Blaeste/libfterator.git
	libfterator/tester.py ./
	rm -rf libfterator/

libftTester : #Tripouille
	git clone git@github.com:Tripouille/libftTester.git
	cd libftTester && make a
	cd ..
	rm -rf libftTester/

libft_fairy :
	git clone git@github.com:gcxd68/libft-fairy.git
	cd libft-fairy/ && ./run.sh
	cd ..
	rm -rf libft-fairy/

libft_unit :
	cd .. && git clone git@github.com:alelievr/libft-unit-test.git
	cd ../libft-unit-test && make f
	cd ../libft-unit-test && ./run_test
	cd ../ && rm -rf libft-unit-test
