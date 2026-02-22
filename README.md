# dbms-program-4

Write a PL/SQL block to delete the record of employee for given EID.


set serveroutput on;

declare

    v_eid emp.eid%type;

begin
    
    v_eid := &enter_eid;

    
    delete from emp where eid = v_eid;

  
    if sql%found then
        dbms_output.put_line('employee record deleted successfully.');
    else
        dbms_output.put_line('employee not found.');
    end if;

    commit;
end;
/
